ģ��ɱ�ӳ�䵽�ļ���Ŀ¼��Ρ������ǰ�[�ɼ���](/mod/visibility.html)ʾ�������ɢ������ļ���

```
$ tree .
.
|-- my
|   |-- inaccessible.rs
|   |-- mod.rs
|   `-- nested.rs
`-- split.rs
```

{split.rs}

{my/mod.rs}

{my/nested.rs}

{my/inaccessible.rs}

����������֮ǰһ������������

```
$ rustc split.rs && ./split
called `my::function()`
called `function()`
called `my::indirect_access()`, that
> called `my::private_function()`
called `my::nested::function()`
```

# prosemirror-history

[ [**WEBSITE**](https://prosemirror.net) | [**ISSUES**](https://github.com/prosemirror/prosemirror/issues) | [**FORUM**](https://discuss.prosemirror.net) | [**GITTER**](https://gitter.im/ProseMirror/prosemirror) | [**CHANGELOG**](https://github.com/ProseMirror/prosemirror-history/blob/master/CHANGELOG.md) ]

This is a [core module](https://prosemirror.net/docs/ref/#history) of [ProseMirror](https://prosemirror.net).
ProseMirror is a well-behaved rich semantic content editor based on
contentEditable, with support for collaborative editing and custom
document schemas.

This [module](https://prosemirror.net/docs/ref/#history) implements an
undo/redo history plugin for ProseMirror.

The [project page](https://prosemirror.net) has more information, a
number of [examples](https://prosemirror.net/examples/) and the
[documentation](https://prosemirror.net/docs/).

This code is released under an
[MIT license](https://github.com/prosemirror/prosemirror/tree/master/LICENSE).
There's a [forum](http://discuss.prosemirror.net) for general
discussion and support requests, and the
[Github bug tracker](https://github.com/prosemirror/prosemirror/issues)
is the place to report issues.

We aim to be an inclusive, welcoming community. To make that explicit,
we have a [code of
conduct](http://contributor-covenant.org/version/1/1/0/) that applies
to communication around the project.

修改原始的undo redo逻辑, 记录每次修改前后的选区, 用于redo时选区的恢复, 替代原始的当前state的 state.selection.getBookmark

执行undo前更改选区位置, 将不会对重做后的选区造成影响

Modify undo/redo logic. Record old and new selection when doc was changed instead of state.selection.getBookmark()

Selection will not be affected by the selection changing before executing undo
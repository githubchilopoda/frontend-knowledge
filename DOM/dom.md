# why

DOM中的原生方法拥有最好的性能，如果要造轮子，必须要会DOM的方法

# nodeType

Constant | Value
---|---
Node.ELEMENT_NODE | 1
Node.TEXT_NODE | 3
Node.COMMENT_NODE | 8
Node.DOCUMENT_NODE | 9

https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeType

# dom ready

```js
document.addEventListener("DOMContentLoaded", function(event) {
    console.log("DOM fully loaded and parsed");
});
```

# TreeWalker

```js
function walkTree(node, callback) {
    var treeWalker = document.createTreeWalker(node, NodeFilter.SHOW_ELEMENT, null, false)
    while (treeWalker.nextNode() != null) {
        callback(treeWalker.currentNode)
    }
}
```
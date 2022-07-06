# babel-plugin-inline-file

In most case, webpack will remove comments while minify code, though some certain configtion could been set to retain some comments, But `edge-js` use standard anotation "/* */" to inject C# code, it's difficult to keep the C# code comments only。

This plugin is target to inject C# code for edge-js。

## js
```
edge.func({
    source: function(){__inline("camera.cs")},
    references: [
        path.join(__static, "face/Intel.RealSense.dll")
    ],
})
```

## camera.cs
```
/*
#r "System.Drawing.dll"
using System;
using System.Drawing;
using Intel.RealSense;
using System.Threading.Tasks;

//some code

*/
```

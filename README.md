# babel-plugin-inline-file

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

## install

```
yarn add babel-plugin-inline-file -D
```


## .babelrc
```
{
    "plugins": [
        "babel-plugin-inline-file"
    ]
}

```

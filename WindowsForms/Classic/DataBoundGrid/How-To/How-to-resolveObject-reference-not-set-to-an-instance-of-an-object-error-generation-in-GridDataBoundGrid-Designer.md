---
layout: post
title: How-to-resolveObject-reference-not-set-to-an-instance of an object | Windows Forms | Syncfusion
description: how to resolve object reference not set to an instance of an object error generation in griddataboundgrid designer
platform: windowsforms
control: DataBoundGrid
documentation: ug
---

## How to Resolve “Object Reference Not Set to an Instance of an Object” Error Generation in GridDataBoundGrid Designer

GridDataBoundGrid is a grid that is bound to data sources such as Data Tables, String Collections, Data Sets, and Data Views. The Hidden, Position and Width properties of GridDataBoundColumn generate the “Object reference not set to an instance of an object” error on designer code generation. This issue has been resolved for version 10.1.0.44 and following versions by setting DesignerSerializationVisibility for these codes to Hidden. However, if the application is migrated from version 9.4.0.62 or earlier versions to the latest version, the designer code throws this exception. This can be fixed by removing the “DesignerSerializationVisibility” part of code from the designer.


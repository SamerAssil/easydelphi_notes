---
title: اضافة body إلى طلب TNetHttpClient
draft: false
tags:
  - fmx
  - vcl
  - TNetHttpClient
---

نوع الـ Body يجب ان يكون TStringList حتى يتم قبوله كـ Body للطلب

مثال: 

```pascal
var
	StrL: TStringList;

begin
...
  ContentType := 'application/json';

  StrL := TStringList.Create;
  try
    StrL.values['query'] := aQuery;
    StrL.values['Variables'] := aVariables;

  res := Self.Post( url, StrL );

```

---
title: "اضافة body إلى طلب TNetHttpClient"
date: 2023-04-25T13:53:44+03:00
draft: false
author: "سامر أصيل"
emoji: 💡
tags:
- fmx
- vcl
- TNetHttpClient


summary: "كيف يتم اضافة الجزء Body إلى TNetHttpClient request"
---

نوع الـ Body يجب ان يكون TStringList حتى يتم قبوله كـ Body للطلب

مثال: 

```Pascal
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
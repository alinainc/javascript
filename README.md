# Alina JavaScript Style Guide
Please read [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript) first. Our rules overrides those rules.

## Table of Contents
1. [Modules](#modules)

## Modules

  <a name="modules--do-not-wrap"></a><a name="1.1"></a>
  - [1.1](#modules--do-not-wrap) **Do not wrap if possible.**
  
  ```javascript
  // good
  import { a, b, c, d, e } from 'module';
  
  // bad
  import {
    a, b, c, d, e,
  } from 'module';
  
  // bad
  import {
    a,
    b,
    c,
    d,
    e,
  } from 'module';
  ```
  
  <a name="modules--alphabetical-order"></a><a name="1.2"></a>
  - [1.2](#modules--alphabetical-order) **Alphbetical order.**
  ```javascript
  // good
  import { A, B, a, b, c } from 'module';
  
  // bad
  import { A, a, B, b, c } from 'module';
  
  // bad
  import { a, b, c, A, B } from 'module';
  ```
  
  <a name="modules--maximum-modules"></a><a name="1.3"></a>
  - [1.3](#modules--maximum-modules) **Wrap if the number of modules is bigger than 5.**
  ```javascript
  // good
  import {
    a, b, c, d, e, f, g,
  } from 'module';
  
  // bad
  import { a, b, c, d, e, f, g } from 'module';
  
  // bad
  import {
    a, b, c, d, e,
    f, g,
  } from 'module';
  ```
  
  <a name="modules--long-modules"></a><a name="1.4"></a>
  - [1.4](#modules--long-modules) **Long name modules.**
  ```javascript
  // good
  import {
    longName, longLongName, longLongLongName, longLongLongLongName, longLongLongLongLongName,
    ultraHifiMiracleCaptshongJjangLongName,
  } from 'module';
  
  // bad
  import {
    longName,
    longLongName,
    longLongLongName,
    longLongLongLongName,
    longLongLongLongLongName,
    ultraHifiMiracleCaptshongJjangLongName,
  } from 'module';
  
  // bad
  import {
    longName, longLongName, longLongLongName,
    longLongLongLongName, longLongLongLongLongName,
    ultraHifiMiracleCaptshongJjangLongName,
  } from 'module';
  ```
  
**[⬆ back to top](#table-of-contents)**

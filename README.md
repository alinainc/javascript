# Alina JavaScript Style Guide
Please read [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript) first. Our rules overrides those rules.

## Table of Contents
1. [Modules](#modules)
1. [GraphQL](#graphql)

## Modules

  <a name="modules--named-imports-order"></a><a name="1.1"></a>
  - [1.1](#modules--named-imports-order) **Put named imports in alphbetical order.**

  ```javascript
  // good
  import { A, B, a, b, c } from 'module';

  // bad
  import { A, a, B, b, c } from 'module';

  // bad
  import { a, b, c, A, B } from 'module';
  ```

  <a name="modules--named-imports"></a><a name="1.2"></a>
  - [1.2](#modules--named-imports) **Put modules in alphbetical order.**

  ```javascript
  // good
  import { b } from 'A';
  import { c } from 'B';
  import { a } from 'C';

  // bad
  import { a } from 'C';
  import { b } from 'A';
  import { c } from 'B';
  ```

   <a name="modules--do-not-wrap"></a><a name="1.3"></a>
  - [1.3](#modules--do-not-wrap) **Do not wrap unless it is necessary.**

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

  <a name="modules--maximum-modules"></a><a name="1.4"></a>
  - [1.4](#modules--maximum-modules) **Wrap if the number of named imports is more than 5.**

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

  <a name="modules--long-modules"></a><a name="1.5"></a>
  - [1.5](#modules--long-modules) **Wrap lines exceeding 100 characters.**

  ```javascript
  // good
  import {
    longLongLongLong1, longLongLongLong2, longLongLongLong3, longLongLongLong4,
    veryLongLongLongLong5,
  } from 'module';

  // bad
  import {
    longLongLongLong1, longLongLongLong2, longLongLongLong3, longLongLongLong4, veryLongLongLongLong5,
  } from 'module';
  ```

  <a name="modules--long-modules"></a><a name="1.6"></a>
  - [1.6](#modules--long-modules) **Group modules by module type.**

  1. Node modules and npm modules.
  2. Absolute path modules.
  3. Relative path modules.

  ```javascript
  // good
  import http from 'http';
  import lodash from 'lodash';

  import UserForm from 'components/UserForm';
  import UserList from 'containers/UserList';

  import util from './util';

  // bad
  import http from 'http';
  import lodash from 'lodash';
  import UserForm from 'components/UserForm';
  import UserList from 'containers/UserList';
  import util from './util';

  // bad
  import util from './util';

  import UserForm from 'components/UserForm';
  import UserList from 'containers/UserList';

  import http from 'http';
  import lodash from 'lodash';
  ```

## GraphQL

  <a name="graphql--types"></a><a name="2.1"></a>
  - [2.1](#graphql--types) **Put types in alphbetical order.**

  ```graphql
  # good
  extend type Mutation {}
  extend type Query {}

  #good
  type Employee {}
  type Staff {}

  # bad - Mutation sholud be before Query.
  extend type Query {}
  extend type Mutation {}

  # bad - Employee be before Staff.
  type Staff {}
  type Employee {}
  ```

  <a name="graphql--type-group"></a><a name="2.2"></a>
  - [2.2](#graphql--type-group) **Group types, sort them in alphbetical order and add an empty line between each group.**

  ```graphql
  # good
  extend type Mutation {}
  extend type Query {}

  input EmployeeInput {}

  type Employee {}
  type Staff {}

  # bad - Extend types sholud be before input.
  input EmployeeInput {}

  extend type Mutation {}
  extend type Query {}

  # bad - Empty lines are required between each group.
  extend type Mutation {}
  extend type Query {}
  input EmployeeInput {}
  type Employee {}
  ```

  <a name="graphql--fields"></a><a name="2.3"></a>
  - [2.3](#graphql--fields) **Put fields in alphbetical order.**

  ```graphql
  # good
  extend type Mutation {
    createStaff: Staff!
    updateEmployee: Employee!
  }

  # bad
  extend type Mutation {
    updateEmployee: Employee!
    createStaff: Staff!
  }
  ```

  <a name="graphql--operation-names"></a><a name="2.4"></a>
  - [2.4](#graphql--operation-names) **Operation names are all capital letters with underscores and use same names of the queries or mutations.**

  ```graphql
  # good
  query EMPLOYEE {
    employee { ... }
  }

  # bad
  query Employee {
    employee { ... }
  }

  # bad
  query LOAD_EMPLOYEE {
    employee { ... }
  }
  ```

**[⬆ back to top](#table-of-contents)**

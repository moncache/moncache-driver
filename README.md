# moncache-driver
MonCache driver

### Document / *null*
```json
{"field": null}
```

Globals based presentation:
```lisp
("field", "t") = "null"
```

### Document / *true*
```js
{"field": true}
```

Globals based presentation:
```lisp
("field", "t") = "boolean"
("field", "v") = "true"
```

### Document / *false*
```js
{"field": false}
```

Globals based presentation:
```lisp
("field", "t") = "boolean"
("field", "v") = "false"
```

### Document / *number*
```js
{"field": 1234567890}
```

Globals based presentation:
```lisp
("field", "t") = "number"
("field", "v") = 1234567890
```

### Document / *string*
```js
{"field": "Cogito ergo sum"}
```

Globals based presentation:
```lisp
("field", "t") = "string"
("field", "v") = "Cogito ergo sum"
```

### Document / *ObjectId*
```js
{"field": ObjectId("51e062189c6ae665454e301d")}
```

Globals based presentation:
```lisp
("field", "t") = "objectid"
("field", "v") = "51e062189c6ae665454e301d"
```

### Document / *Empty object*
```js
{"field": {}}
```

Globals based presentation:
```lisp
("field", "t") = "object"
```

### Document / *object*
```js
{"user": {
  "id": 1,
  "login": "jxcoder"
}}
```

Globals based presentation:
```lisp
("user", "t") = "object"

("user", "v", "id", "t") = "number"
("user", "v", "id", "v") = 1

("user", "v", "login", "t") = "string"
("user", "v", "login", "v") = "jxcoder"
```

### Document / *array*
```js
{"user": [1, "jxcoder"]}
```

Globals based presentation:
```lisp
("user", "t") = "array"

("user", "v", 0, "t") = "number"
("user", "v", 0, "v") = 1

("user", "v", 1, "t") = "string"
("user", "v", 1, "v") = "jxcoder"
```

### JSON / *object* in *array*
```js
{"points": [
  {
    "x", 1.23,
    "y": 4.56
  },
  {
    "x": 7.89,
    "y": 0.12
  }
]}
```

Globals based presentation:
```lisp
("user", "t") = "array"

("user", "v", 0, "t") = "object"

("user", "v", 0, "v", "x", "t") = "number"
("user", "v", 0, "v", "x", "v") = 1.23

("user", "v", 0, "v", "y", "t") = "number"
("user", "v", 0, "v", "y", "v") = 4.56

("user", "v", 1, "t") = "object"

("user", "v", 1, "v", "x", "t") = "number"
("user", "v", 1, "v", "x", "v") = 7.89

("user", "v", 1, "v", "y", "t") = "number"
("user", "v", 1, "v", "y", "v") = 0.12
```

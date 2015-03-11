# moncache-driver
MonCache driver

### JSON / **null** field:
```json
{"field": null}
```

Globals based presentation:
```lisp
("field", "t") = "null"
```

### JSON / **true** field:
```json
{"field": true}
```

Globals based presentation:
```lisp
("field", "t") = "boolean"
("field", "v") = "true"
```

### JSON / **false** field:
```json
{"field": false}
```

Globals based presentation:
```lisp
("field", "t") = "boolean"
("field", "v") = "false"
```

### JSON / **number** field:
```json
{"field": 1234567890}
```

Globals based presentation:
```lisp
("field", "t") = "number"
("field", "v") = 1234567890
```

### JSON / **string** field:
```json
{"field": "Cogito ergo sum"}
```

Globals based presentation:
```lisp
("field", "t") = "string"
("field", "v") = "Cogito ergo sum"
```

### JSON / Empty **object** field:
```json
{"field": {}}
```

Globals based presentation:
```lisp
("field", "t") = "object"
```

### JSON / **object** field:
```json
{"user": {"id": 1, "login": "jxcoder"}}
```

Globals based presentation:
```lisp
("user", "t") = "object"
("user", "v", "id", "t") = "number"
("user", "v", "id", "v") = 1
("user", "v", "login", "t") = "string"
("user", "v", "login", "v") = "jxcoder"
```

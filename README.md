# moncache-driver
MonCache driver

# JSON / **null** field:
```json
{"field": null}
```

Globals based presentation:
```lisp
("field", "t") = "null"
```

JSON / **true** field:
```json
{"field": true}
```

Globals based presentation:
```lisp
("field", "t") = "boolean"
("field", "v") = "true"
```

JSON / **false** field:
```json
{"field": false}
```

Globals based presentation:
```lisp
("field", "t") = "boolean"
("field", "v") = "false"
```

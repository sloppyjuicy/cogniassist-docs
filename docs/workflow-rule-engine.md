Branching Rule Syntax
=========================================================

The syntax for creating rules is based off of logical expressions evaluating to either True (matching) or False (non- matching). Rules support a small set of data types which can be defined as constants or resolved using the Python object on which the rule is being applied.

  
### Rule Engine Data Type, Compatible Python Types

[`ARRAY`](rule_engine/ast.html#rule_engine.ast.DataType.ARRAY "rule_engine.ast.DataType.ARRAY"), [`list`](https://docs.python.org/3.7/library/stdtypes.html#list "(in Python v3.7)"), [`tuple`](https://docs.python.org/3.7/library/stdtypes.html#tuple "(in Python v3.7)")

[`BOOLEAN`](rule_engine/ast.html#rule_engine.ast.DataType.BOOLEAN "rule_engine.ast.DataType.BOOLEAN"),[`bool`](https://docs.python.org/3.7/library/functions.html#bool "(in Python v3.7)")

[`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME"), [`datetime.date`](https://docs.python.org/3.7/library/datetime.html#datetime.date "(in Python v3.7)"), [`datetime.datetime`](https://docs.python.org/3.7/library/datetime.html#datetime.datetime "(in Python v3.7)")

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT"), [`int`](https://docs.python.org/3.7/library/functions.html#int "(in Python v3.7)"), [`float`](https://docs.python.org/3.7/library/functions.html#float "(in Python v3.7)")

[`NULL`](rule_engine/ast.html#rule_engine.ast.DataType.NULL "rule_engine.ast.DataType.NULL"), `NoneType`

[`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING"),[`str`](https://docs.python.org/3.7/library/stdtypes.html#str "(in Python v3.7)")


Not all supported operations work with all data types as noted in the table below. Rules follow a standard [order of operations](https://en.wikipedia.org/wiki/Order_of_operations#Programming_languages).

Grammar
-------------------------------------------------

The expression grammar supports a number of operations including basic arithmetic for numerical data and regular expressions for strings. Operations are type aware and will raise an exception when an incompatible type is used.

### Supported Operations
The following table outlines all operators that can be used in Rule Engine expressions.

**Arithmetic Operators**

Operation, Description, Compatible Data Types

`+`

Addition

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`-`

Subtraction

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`*`

Multiplication

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`**`

Exponent

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`/`

True division

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`//`

Floor division

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`%`

Modulo

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

**Bitwise-Arithmetic Operators**

`&`

Bitwise-and 1

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`|`

Bitwise-or 1

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`^`

Bitwise-xor 1

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`>>`

Bitwise right shift 1

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

`<<`

Bitwise left shift 1

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")

**Comparison Operators**

`==`

Equal to

_ANY_

`!=`

Not equal to

_ANY_

**Arithmetic-Comparison Operators**

`>`

Greater than

_ANY_ 2

`>=`

Greater than or equal to

_ANY_ 2

`<`

Less than

_ANY_ 2

`<=`

Less than or equal to

_ANY_ 2

**Fuzzy-Comparison Operators**

`=~`

Regex match 3

[`NULL`](rule_engine/ast.html#rule_engine.ast.DataType.NULL "rule_engine.ast.DataType.NULL"), [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING")

`=~~`

Regex search 3

[`NULL`](rule_engine/ast.html#rule_engine.ast.DataType.NULL "rule_engine.ast.DataType.NULL"), [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING")

`!~`

Regex match fails 3

[`NULL`](rule_engine/ast.html#rule_engine.ast.DataType.NULL "rule_engine.ast.DataType.NULL"), [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING")

`!~~`

Regex search fails 3

[`NULL`](rule_engine/ast.html#rule_engine.ast.DataType.NULL "rule_engine.ast.DataType.NULL"), [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING")

**Logical Operators**

`and`

Logical and

_ANY_

`not`

Logical not

_ANY_

`or`

Logical or

_ANY_

1 Bitwise operations support floating point values, but if the value is not a natural number, an [`EvaluationError`](rule_engine/errors.html#rule_engine.errors.EvaluationError "rule_engine.errors.EvaluationError") will be raised.

2 The arithmetic comparison operators support multiple data types however the data type of the left value must be the same as the data type of the right. For example, a [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING") can be compared to another [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING") but not a [`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT"). The technique is the same lexicographical ordering based sequence comparison [technique used by Python](https://docs.python.org/3/tutorial/datastructures.html#comparing-sequences-and-other-types).

3 When using regular expression operations, the expression on the left is the string to compare and the expression on the right is the regular expression to use for either the match or search operation.

### Reserved Keywords

The following keywords are reserved and can not be used as the names of symbols.

  

Keyword, Description

`null`

The [`NullExpression`](rule_engine/ast.html#rule_engine.ast.NullExpression "rule_engine.ast.NullExpression") literal value

**Booleans** ([`BooleanExpression`](rule_engine/ast.html#rule_engine.ast.BooleanExpression "rule_engine.ast.BooleanExpression") Literals)

`true`

The “True” boolean value

`false`

The “False” boolean value

**Floats** ([`FloatExpression`](rule_engine/ast.html#rule_engine.ast.FloatExpression "rule_engine.ast.FloatExpression") Literals)

`inf`

Floating point value for infinity

`nan`

Floating point value for not-a-number

**Logical Operators**

`and`

Logical “and” operator

`not`

Logical “not” operator

`or`

Logical “or” operator

**Membership Operators**

`in`

Checks member is in the container

### Literal Values
[`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME") and [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING") literal values are specified in a very similar manner by defining the value as a string of characters enclosed in either single or double quotes. The difference comes in an optional leading character before the opening quote. Either no leading character or a single `s` will specify a standard [`STRING`](rule_engine/ast.html#rule_engine.ast.DataType.STRING "rule_engine.ast.DataType.STRING") value, while a single `d` will specify a [`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME") value.

[`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME") literals must be specified in ISO-8601 format. The underlying parsing logic is provided by [`dateutil.parser.isoparse()`](https://dateutil.readthedocs.io/en/stable/parser.html#dateutil.parser.isoparse "(in dateutil v2.8.1)"). [`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME") values with no time specified (e.g. `d"2019-09-23"`) will evaluate to a [`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME") of the specified day at exactly midnight.

Example rules showing equivalent literal expressions:

*   `"foobar" == s"foobar"`
    
*   `d"2019-09-23" == d"2019-09-23 00:00:00"`
    

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT") literals may be expressed in either binary, octal, decimal, or hexadecimal formats. The binary, octal and hexadecimal formats use the `0b`, `0o`, and `0x` prefixes respectively. Values in the decimal format require no prefix and is the default base in which values are represented. Only base-10, decimal values may include a decimal place component.

Example rules showing equivalent literal expressions:

*   `0b10 == 2`
    
*   `0o10 == 8`
    
*   `10.0 == 10`
    
*   `0x10 == 16`
    

[`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT") literals may also be expressed in scientific notation using the letter `e`.

Example rules show equivalent literal expressions:

*   `1E0 == 1`
    
*   `1e0 == 1`
    
*   `1.0e0 == 1`
    

Builtin Symbols
-----------------------------------------------------------------

The following symbols are provided by default using the [`from_defaults()`](rule_engine/engine.html#rule_engine.engine.Builtins.from_defaults "rule_engine.engine.Builtins.from_defaults") method. These symbols can be accessed through the `$` prefix, e.g. `$pi`. The default values can be overridden by defining a custom subclass of [`Context`](rule_engine/engine.html#rule_engine.engine.Context "rule_engine.engine.Context") and setting the [`builtins`](rule_engine/engine.html#rule_engine.engine.Context.builtins "rule_engine.engine.Context.builtins") attribute.

### Math Related

*   `e` (type: [`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")) – The mathematical constant _e_ (2.71828…).
    
*   `pi` (type: [`FLOAT`](rule_engine/ast.html#rule_engine.ast.DataType.FLOAT "rule_engine.ast.DataType.FLOAT")) – The mathematical constant _pi_ (3.14159…).
    

### Regular Expression Related

*   `re_groups` (type: [`ARRAY`](rule_engine/ast.html#rule_engine.ast.DataType.ARRAY "rule_engine.ast.DataType.ARRAY")) – An array of strings from the last regular expression match as defined by the regular expression itself. See documentation on [grouping](https://docs.python.org/3/howto/regex.html#grouping) for more information. If no match has taken place, this value is [`NULL`](rule_engine/ast.html#rule_engine.ast.DataType.NULL "rule_engine.ast.DataType.NULL").
    
    Note
    
    For technical reasons, this symbol is provided by the default [`Context`](rule_engine/engine.html#rule_engine.engine.Context "rule_engine.engine.Context") and is not included within the [`from_defaults()`](rule_engine/engine.html#rule_engine.engine.Builtins.from_defaults "rule_engine.engine.Builtins.from_defaults"). This means that unlike the other symbols listed here, it will be unavailable if the default builtins are replaced.
    

### Timestamp Related
*   `now` (type: [`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME")) – The current timestamp (including time) using the default timezone from [`default_timezone`](rule_engine/engine.html#rule_engine.engine.Context.default_timezone "rule_engine.engine.Context.default_timezone").
    
*   `today` (type: [`DATETIME`](rule_engine/ast.html#rule_engine.ast.DataType.DATETIME "rule_engine.ast.DataType.DATETIME")) – The current timestamp, (excluding time, normalized to midnight 00:00:00) using the default timezone from [`default_timezone`](rule_engine/engine.html#rule_engine.engine.Context.default_timezone "rule_engine.engine.Context.default_timezone").
    
* * *

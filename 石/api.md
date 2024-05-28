# Authentication

# wjx/UserController

## POST registerUser

POST /api/users/register

> Body 请求参数

```json
{
  "name": "string",
  "age": 0,
  "gender": 0,
  "phone": "string",
  "password": "string",
  "email": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[UserDto](#schemauserdto)| 否 |none|

> 返回示例

> 成功

```json
null
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|string|

# wjx/SurveyController

## POST createSurvey

POST /api/surveys

> Body 请求参数

```json
{
  "id": 0,
  "title": "string",
  "createdBy": 0,
  "description": "string",
  "createdAt": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[SurveyDto](#schemasurveydto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "title": "",
  "createdBy": 0,
  "description": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«SurveyDto»](#schemaresponseentity«surveydto»)|

## GET getAllSurveys

GET /api/surveys

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "title": "",
    "createdBy": 0,
    "description": ""
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«SurveyDto»](#schemalist«surveydto»)]|false|none||none|
|» id|integer¦null|false|none||none|
|» title|string¦null|false|none||none|
|» createdBy|integer¦null|false|none||none|
|» description|string¦null|false|none||none|
|» createdAt|string¦null|false|none||none|

## GET getSurveyById

GET /api/surveys/{id}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "title": "",
  "createdBy": 0,
  "description": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«SurveyDto»](#schemaresponseentity«surveydto»)|

## PUT updateSurvey

PUT /api/surveys/{id}

> Body 请求参数

```json
{
  "id": 0,
  "title": "string",
  "createdBy": 0,
  "description": "string",
  "createdAt": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|
|body|body|[SurveyDto](#schemasurveydto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "title": "",
  "createdBy": 0,
  "description": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«SurveyDto»](#schemaresponseentity«surveydto»)|

## DELETE deleteSurvey

DELETE /api/surveys/{id}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|

> 返回示例

> 成功

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«?»](#schemaresponseentity«?»)|

## GET getSurveysByUserId

GET /api/surveys/user/{userId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|path|string| 是 |none|

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "title": "",
    "createdBy": 0,
    "description": ""
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«SurveyDto»](#schemalist«surveydto»)]|false|none||none|
|» id|integer¦null|false|none||none|
|» title|string¦null|false|none||none|
|» createdBy|integer¦null|false|none||none|
|» description|string¦null|false|none||none|
|» createdAt|string¦null|false|none||none|

## GET getSurveysByUserIdSorted

GET /api/surveys/user/{userId}/sorted

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|userId|path|string| 是 |none|

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "title": "",
    "createdBy": 0,
    "description": "",
    "createdAt": ""
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«SurveyDto»](#schemalist«surveydto»)]|false|none||none|
|» id|integer¦null|false|none||none|
|» title|string¦null|false|none||none|
|» createdBy|integer¦null|false|none||none|
|» description|string¦null|false|none||none|
|» createdAt|string¦null|false|none||none|

# wjx/ResponseController

## POST addResponseToQuestion

POST /api/responses/{questionId}

> Body 请求参数

```json
{
  "id": 0,
  "questionId": 0,
  "answerText": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|
|body|body|[ResponseDto](#schemaresponsedto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "questionId": 0,
  "answerText": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«ResponseDto»](#schemaresponseentity«responsedto»)|

## GET getResponsesForQuestion

GET /api/responses/{questionId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "questionId": 0,
    "answerText": ""
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«ResponseDto»](#schemalist«responsedto»)]|false|none||none|
|» id|integer¦null|false|none||none|
|» questionId|integer¦null|false|none||none|
|» answerText|string¦null|false|none||none|

## DELETE deleteResponse

DELETE /api/responses/{id}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|

> 返回示例

> 成功

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«?»](#schemaresponseentity«?»)|

# wjx/QuestionController

## POST addQuestion

POST /api/surveys/{surveyId}/questions

> Body 请求参数

```json
{
  "id": 0,
  "text": "string",
  "type": "string",
  "surveyId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|surveyId|path|string| 是 |none|
|body|body|[Question](#schemaquestion)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "text": "",
  "type": "",
  "surveyId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«Question»](#schemaresponseentity«question»)|

## GET getAllQuestionsBySurveyId

GET /api/surveys/{surveyId}/questions

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|surveyId|path|string| 是 |none|

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "text": "",
    "type": "",
    "surveyId": 0
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«Question»](#schemalist«question»)]|false|none||none|
|» id|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.id|
|» text|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.text|
|» type|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.type|
|» surveyId|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.survey_id|

## GET getQuestionById

GET /api/surveys/{surveyId}/questions/{questionId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "text": "",
  "type": "",
  "surveyId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«Question»](#schemaresponseentity«question»)|

## PUT updateQuestion

PUT /api/surveys/{surveyId}/questions/{questionId}

> Body 请求参数

```json
{
  "id": 0,
  "text": "string",
  "type": "string",
  "surveyId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|
|body|body|[Question](#schemaquestion)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "text": "",
  "type": "",
  "surveyId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«Question»](#schemaresponseentity«question»)|

## DELETE deleteQuestion

DELETE /api/surveys/{surveyId}/questions/{questionId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## GET getOptionsForQuestion

GET /api/surveys/{surveyId}/questions/{questionId}/options

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "optionText": "",
    "questionId": 0
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«OptionDto»](#schemalist«optiondto»)]|false|none||none|
|» id|integer¦null|false|none||none|
|» optionText|string¦null|false|none||none|
|» questionId|integer¦null|false|none||none|

## POST addOption

POST /api/surveys/{surveyId}/questions/{questionId}/options

> Body 请求参数

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|
|body|body|[OptionDto](#schemaoptiondto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "optionText": "",
  "questionId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«OptionDto»](#schemaresponseentity«optiondto»)|

## PUT updateOption

PUT /api/surveys/{surveyId}/questions/{questionId}/options/{optionId}

> Body 请求参数

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|
|optionId|path|string| 是 |none|
|body|body|[OptionDto](#schemaoptiondto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "optionText": "",
  "questionId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«OptionDto»](#schemaresponseentity«optiondto»)|

# wjx/OptionController

## POST addOptionToQuestion

POST /api/options/{questionId}

> Body 请求参数

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|
|body|body|[OptionDto](#schemaoptiondto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "optionText": "",
  "questionId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«OptionDto»](#schemaresponseentity«optiondto»)|

## GET getOptionsForQuestion

GET /api/options/{questionId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|questionId|path|string| 是 |none|

> 返回示例

> 成功

```json
[
  {
    "id": 0,
    "optionText": "",
    "questionId": 0
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[List«OptionDto»](#schemalist«optiondto»)]|false|none||none|
|» id|integer¦null|false|none||none|
|» optionText|string¦null|false|none||none|
|» questionId|integer¦null|false|none||none|

## PUT updateOption

PUT /api/options/{id}

> Body 请求参数

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|
|body|body|[OptionDto](#schemaoptiondto)| 否 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "optionText": "",
  "questionId": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«OptionDto»](#schemaresponseentity«optiondto»)|

## DELETE deleteOption

DELETE /api/options/{id}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|

> 返回示例

> 成功

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«?»](#schemaresponseentity«?»)|

# wjx/LoginController

## POST login

POST /api/users/login

> Body 请求参数

```json
{
  "email": "string",
  "password": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[LoginDto](#schemalogindto)| 否 |none|

> 返回示例

> 成功

```json
{
  "token": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|[ResponseEntity«LoginResponse»](#schemaresponseentity«loginresponse»)|

# 数据模型

<h2 id="tocS_OptionDto">OptionDto</h2>

<a id="schemaoptiondto"></a>
<a id="schema_OptionDto"></a>
<a id="tocSoptiondto"></a>
<a id="tocsoptiondto"></a>

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|optionText|string¦null|false|none||none|
|questionId|integer¦null|false|none||none|

<h2 id="tocS_ResponseEntity«OptionDto»">ResponseEntity«OptionDto»</h2>

<a id="schemaresponseentity«optiondto»"></a>
<a id="schema_ResponseEntity«OptionDto»"></a>
<a id="tocSresponseentity«optiondto»"></a>
<a id="tocsresponseentity«optiondto»"></a>

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|optionText|string¦null|false|none||none|
|questionId|integer¦null|false|none||none|

<h2 id="tocS_List«OptionDto»">List«OptionDto»</h2>

<a id="schemalist«optiondto»"></a>
<a id="schema_List«OptionDto»"></a>
<a id="tocSlist«optiondto»"></a>
<a id="tocslist«optiondto»"></a>

```json
{
  "id": 0,
  "optionText": "string",
  "questionId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|optionText|string¦null|false|none||none|
|questionId|integer¦null|false|none||none|

<h2 id="tocS_ResponseEntity«?»">ResponseEntity«?»</h2>

<a id="schemaresponseentity«?»"></a>
<a id="schema_ResponseEntity«?»"></a>
<a id="tocSresponseentity«?»"></a>
<a id="tocsresponseentity«?»"></a>

```json
{}

```

### 属性

*None*

<h2 id="tocS_List«Question»">List«Question»</h2>

<a id="schemalist«question»"></a>
<a id="schema_List«Question»"></a>
<a id="tocSlist«question»"></a>
<a id="tocslist«question»"></a>

```json
{
  "id": 0,
  "text": "string",
  "type": "string",
  "surveyId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.id|
|text|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.text|
|type|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.type|
|surveyId|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.survey_id|

<h2 id="tocS_List«ResponseDto»">List«ResponseDto»</h2>

<a id="schemalist«responsedto»"></a>
<a id="schema_List«ResponseDto»"></a>
<a id="tocSlist«responsedto»"></a>
<a id="tocslist«responsedto»"></a>

```json
{
  "id": 0,
  "questionId": 0,
  "answerText": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|questionId|integer¦null|false|none||none|
|answerText|string¦null|false|none||none|

<h2 id="tocS_List«SurveyDto»">List«SurveyDto»</h2>

<a id="schemalist«surveydto»"></a>
<a id="schema_List«SurveyDto»"></a>
<a id="tocSlist«surveydto»"></a>
<a id="tocslist«surveydto»"></a>

```json
{
  "id": 0,
  "title": "string",
  "createdBy": 0,
  "description": "string",
  "createdAt": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|title|string¦null|false|none||none|
|createdBy|integer¦null|false|none||none|
|description|string¦null|false|none||none|
|createdAt|string¦null|false|none||none|

<h2 id="tocS_Tag">Tag</h2>

<a id="schematag"></a>
<a id="schema_Tag"></a>
<a id="tocStag"></a>
<a id="tocstag"></a>

```json
{
  "id": 1,
  "name": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||标签ID编号|
|name|string|false|none||标签名称|

<h2 id="tocS_LoginDto">LoginDto</h2>

<a id="schemalogindto"></a>
<a id="schema_LoginDto"></a>
<a id="tocSlogindto"></a>
<a id="tocslogindto"></a>

```json
{
  "email": "string",
  "password": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|email|string¦null|false|none||none|
|password|string¦null|false|none||none|

<h2 id="tocS_Question">Question</h2>

<a id="schemaquestion"></a>
<a id="schema_Question"></a>
<a id="tocSquestion"></a>
<a id="tocsquestion"></a>

```json
{
  "id": 0,
  "text": "string",
  "type": "string",
  "surveyId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.id|
|text|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.text|
|type|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.type|
|surveyId|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.survey_id|

<h2 id="tocS_ResponseDto">ResponseDto</h2>

<a id="schemaresponsedto"></a>
<a id="schema_ResponseDto"></a>
<a id="tocSresponsedto"></a>
<a id="tocsresponsedto"></a>

```json
{
  "id": 0,
  "questionId": 0,
  "answerText": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|questionId|integer¦null|false|none||none|
|answerText|string¦null|false|none||none|

<h2 id="tocS_SurveyDto">SurveyDto</h2>

<a id="schemasurveydto"></a>
<a id="schema_SurveyDto"></a>
<a id="tocSsurveydto"></a>
<a id="tocssurveydto"></a>

```json
{
  "id": 0,
  "title": "string",
  "createdBy": 0,
  "description": "string",
  "createdAt": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|title|string¦null|false|none||none|
|createdBy|integer¦null|false|none||none|
|description|string¦null|false|none||none|
|createdAt|string¦null|false|none||none|

<h2 id="tocS_Category">Category</h2>

<a id="schemacategory"></a>
<a id="schema_Category"></a>
<a id="tocScategory"></a>
<a id="tocscategory"></a>

```json
{
  "id": 1,
  "name": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||分组ID编号|
|name|string|false|none||分组名称|

<h2 id="tocS_ResponseEntity«LoginResponse»">ResponseEntity«LoginResponse»</h2>

<a id="schemaresponseentity«loginresponse»"></a>
<a id="schema_ResponseEntity«LoginResponse»"></a>
<a id="tocSresponseentity«loginresponse»"></a>
<a id="tocsresponseentity«loginresponse»"></a>

```json
{
  "token": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|token|string¦null|false|none||none|

<h2 id="tocS_ResponseEntity«Question»">ResponseEntity«Question»</h2>

<a id="schemaresponseentity«question»"></a>
<a id="schema_ResponseEntity«Question»"></a>
<a id="tocSresponseentity«question»"></a>
<a id="tocsresponseentity«question»"></a>

```json
{
  "id": 0,
  "text": "string",
  "type": "string",
  "surveyId": 0
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.id|
|text|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.text|
|type|string¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.type|
|surveyId|integer¦null|false|none||This field was generated by MyBatis Generator.<br />This field corresponds to the database column questions.survey_id|

<h2 id="tocS_ResponseEntity«ResponseDto»">ResponseEntity«ResponseDto»</h2>

<a id="schemaresponseentity«responsedto»"></a>
<a id="schema_ResponseEntity«ResponseDto»"></a>
<a id="tocSresponseentity«responsedto»"></a>
<a id="tocsresponseentity«responsedto»"></a>

```json
{
  "id": 0,
  "questionId": 0,
  "answerText": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|questionId|integer¦null|false|none||none|
|answerText|string¦null|false|none||none|

<h2 id="tocS_ResponseEntity«SurveyDto»">ResponseEntity«SurveyDto»</h2>

<a id="schemaresponseentity«surveydto»"></a>
<a id="schema_ResponseEntity«SurveyDto»"></a>
<a id="tocSresponseentity«surveydto»"></a>
<a id="tocsresponseentity«surveydto»"></a>

```json
{
  "id": 0,
  "title": "string",
  "createdBy": 0,
  "description": "string",
  "createdAt": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer¦null|false|none||none|
|title|string¦null|false|none||none|
|createdBy|integer¦null|false|none||none|
|description|string¦null|false|none||none|
|createdAt|string¦null|false|none||none|

<h2 id="tocS_UserDto">UserDto</h2>

<a id="schemauserdto"></a>
<a id="schema_UserDto"></a>
<a id="tocSuserdto"></a>
<a id="tocsuserdto"></a>

```json
{
  "name": "string",
  "age": 0,
  "gender": 0,
  "phone": "string",
  "password": "string",
  "email": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|name|string¦null|false|none||none|
|age|number¦null|false|none||none|
|gender|number¦null|false|none||none|
|phone|string¦null|false|none||none|
|password|string¦null|false|none||none|
|email|string¦null|false|none||none|

<h2 id="tocS_Pet">Pet</h2>

<a id="schemapet"></a>
<a id="schema_Pet"></a>
<a id="tocSpet"></a>
<a id="tocspet"></a>

```json
{
  "id": 1,
  "category": {
    "id": 1,
    "name": "string"
  },
  "name": "doggie",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 1,
      "name": "string"
    }
  ],
  "status": "available"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|true|none||宠物ID编号|
|category|[Category](#schemacategory)|true|none||分组|
|name|string|true|none||名称|
|photoUrls|[string]|true|none||照片URL|
|tags|[[Tag](#schematag)]|true|none||标签|
|status|string|true|none||宠物销售状态|

#### 枚举值

|属性|值|
|---|---|
|status|available|
|status|pending|
|status|sold|


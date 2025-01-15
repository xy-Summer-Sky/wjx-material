# wjx

Base URLs:

# Authentication

# LoginController

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

# OptionController

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|*anonymous*|[[List«OptionDto»](#schemalist%c2%aboptiondto%c2%bb)]|false|none||none|

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## GET getOptionsByQuestionId

GET /api/options/question/{questionId}

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
|*anonymous*|[[List«OptionDto»](#schemalist%c2%aboptiondto%c2%bb)]|false|none||none|

# QuestionController

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|*anonymous*|[[List«Question»](#schemalist%c2%abquestion%c2%bb)]|false|none||none|

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|*anonymous*|[[List«OptionDto»](#schemalist%c2%aboptiondto%c2%bb)]|false|none||none|

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
|surveyId|path|string| 是 |none|
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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

# ResponseController

## POST addResponseToQuestion

POST /api/responses/{questionId}

> Body 请求参数

```json
{
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
  "questionId": 0,
  "answerText": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|*anonymous*|[[List«ResponseDto»](#schemalist%c2%abresponsedto%c2%bb)]|false|none||none|

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

# SurveyController

## POST createSurvey

POST /api/surveys/create

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
  "description": "",
  "createdAt": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
  "description": "",
  "createdAt": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
  "description": "",
  "createdAt": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

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
|*anonymous*|[[List«SurveyDto»](#schemalist%c2%absurveydto%c2%bb)]|false|none||none|

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
|*anonymous*|[[List«SurveyDto»](#schemalist%c2%absurveydto%c2%bb)]|false|none||none|

## GET downloadSurveyResponses

GET /api/surveys/responses/download/{surveyId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|surveyId|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "inputStream": {},
  "description": "",
  "read": false
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## GET getSurveyState

GET /api/surveys/state/{surveyId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|surveyId|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## PUT incrementSurveyState

PUT /api/surveys/state/addNum/{surveyId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|surveyId|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## PUT changeSurveyState

PUT /api/surveys/state/changeSurveyState/{surveyId}

> Body 请求参数

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[SurveyStateDto](#schemasurveystatedto)| 否 |none|

> 返回示例

> 成功

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

## POST addSurveyState

POST /api/surveys/addState/{surveyId}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|surveyId|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

# UserController

## POST registerUser

POST /api/users/register

> Body 请求参数

```json
{
  "id": 0,
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

## GET getUserId

GET /api/users/getUserId

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|email|query|string| 是 |none|

> 返回示例

> 成功

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|integer|

## GET getUserById

GET /api/users/getUserById/{id}

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|string| 是 |none|

> 返回示例

> 成功

```json
{
  "id": 0,
  "name": "",
  "age": 0,
  "gender": 0,
  "phone": "",
  "password": "",
  "email": ""
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|成功|Inline|

### 返回数据结构

# 数据模型

<h2 id="tocS_SurveyStateDto">SurveyStateDto</h2>

<a id="schemasurveystatedto"></a>
<a id="schema_SurveyStateDto"></a>
<a id="tocSsurveystatedto"></a>
<a id="tocssurveystatedto"></a>

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|surveyId|integer¦null|false|none||none|
|receivenumber|integer¦null|false|none||none|
|state|string¦null|false|none||none|

<h2 id="tocS_ResponseEntity«SurveyStateDto»">ResponseEntity«SurveyStateDto»</h2>

<a id="schemaresponseentity«surveystatedto»"></a>
<a id="schema_ResponseEntity«SurveyStateDto»"></a>
<a id="tocSresponseentity«surveystatedto»"></a>
<a id="tocsresponseentity«surveystatedto»"></a>

```json
{
  "surveyId": 0,
  "receivenumber": 0,
  "state": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|surveyId|integer¦null|false|none||none|
|receivenumber|integer¦null|false|none||none|
|state|string¦null|false|none||none|

<h2 id="tocS_ResponseEntity«InputStreamResource»">ResponseEntity«InputStreamResource»</h2>

<a id="schemaresponseentity«inputstreamresource»"></a>
<a id="schema_ResponseEntity«InputStreamResource»"></a>
<a id="tocSresponseentity«inputstreamresource»"></a>
<a id="tocsresponseentity«inputstreamresource»"></a>

```json
{
  "inputStream": {},
  "description": "string",
  "read": true
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|inputStream|[InputStream](#schemainputstream)|false|none||none|
|description|string¦null|false|none||none|
|read|boolean¦null|false|none||none|

<h2 id="tocS_InputStream">InputStream</h2>

<a id="schemainputstream"></a>
<a id="schema_InputStream"></a>
<a id="tocSinputstream"></a>
<a id="tocsinputstream"></a>

```json
{}

```

### 属性

*None*

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

<h2 id="tocS_List«ResponseDto»">List«ResponseDto»</h2>

<a id="schemalist«responsedto»"></a>
<a id="schema_List«ResponseDto»"></a>
<a id="tocSlist«responsedto»"></a>
<a id="tocslist«responsedto»"></a>

```json
{
  "questionId": 0,
  "answerText": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|questionId|integer¦null|false|none||none|
|answerText|string¦null|false|none||none|

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

<h2 id="tocS_ResponseEntity«UserDto»">ResponseEntity«UserDto»</h2>

<a id="schemaresponseentity«userdto»"></a>
<a id="schema_ResponseEntity«UserDto»"></a>
<a id="tocSresponseentity«userdto»"></a>
<a id="tocsresponseentity«userdto»"></a>

```json
{
  "id": 0,
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
|id|integer¦null|false|none||none|
|name|string¦null|false|none||none|
|age|number¦null|false|none||none|
|gender|number¦null|false|none||none|
|phone|string¦null|false|none||none|
|password|string¦null|false|none||none|
|email|string¦null|false|none||none|

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

<h2 id="tocS_ResponseDto">ResponseDto</h2>

<a id="schemaresponsedto"></a>
<a id="schema_ResponseDto"></a>
<a id="tocSresponsedto"></a>
<a id="tocsresponsedto"></a>

```json
{
  "questionId": 0,
  "answerText": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|questionId|integer¦null|false|none||none|
|answerText|string¦null|false|none||none|

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

<h2 id="tocS_UserDto">UserDto</h2>

<a id="schemauserdto"></a>
<a id="schema_UserDto"></a>
<a id="tocSuserdto"></a>
<a id="tocsuserdto"></a>

```json
{
  "id": 0,
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
|id|integer¦null|false|none||none|
|name|string¦null|false|none||none|
|age|number¦null|false|none||none|
|gender|number¦null|false|none||none|
|phone|string¦null|false|none||none|
|password|string¦null|false|none||none|
|email|string¦null|false|none||none|

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

<h2 id="tocS_ResponseEntity«ResponseDto»">ResponseEntity«ResponseDto»</h2>

<a id="schemaresponseentity«responsedto»"></a>
<a id="schema_ResponseEntity«ResponseDto»"></a>
<a id="tocSresponseentity«responsedto»"></a>
<a id="tocsresponseentity«responsedto»"></a>

```json
{
  "questionId": 0,
  "answerText": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|questionId|integer¦null|false|none||none|
|answerText|string¦null|false|none||none|

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


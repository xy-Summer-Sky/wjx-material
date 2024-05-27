这里是一个使用Markdown格式编写的API文档示例，它适用于 `OptionController` 类。这个文档清晰地描述了每个API端点的详细信息，包括请求方法、路径、参数及预期的响应。

## API 文档 - 选项管理

### 1. 给某个问题添加选项

- **Endpoint**: `POST /api/options/{questionId}`
- **URL Parameters**:
  - `questionId` (required): 问题的唯一标识符。
- **Request Body**: JSON 格式的 `OptionDto` 对象，示例:
  ```json
  {
    "text": "选项文本"
  }
  ```
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 1,
      "text": "选项文本",
      "questionId": 1
    }
    ```
- **Error Response**:
  - **Code**: `400 Bad Request`
  - **Content**: `{ "error": "错误信息" }`

### 2. 根据问题ID获取选项

- **Endpoint**: `GET /api/options/{questionId}`
- **URL Parameters**:
  - `questionId` (required): 问题的唯一标识符。
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    [
      {
        "id": 1,
        "text": "选项文本",
        "questionId": 1
      },
      {
        "id": 2,
        "text": "选项文本2",
        "questionId": 1
      }
    ]
    ```
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "错误信息" }`

### 3. 根据选项ID更新选项

- **Endpoint**: `PUT /api/options/{id}`
- **URL Parameters**:
  - `id` (required): 选项的唯一标识符。
- **Request Body**: JSON 格式的 `OptionDto` 对象，示例:
  ```json
  {
    "text": "更新后的选项文本"
  }
  ```
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 1,
      "text": "更新后的选项文本",
      "questionId": 1
    }
    ```
- **Error Response**:
  - **Code**: `400 Bad Request`
  - **Content**: `{ "error": "错误信息" }`

### 4. 根据选项ID删除选项

- **Endpoint**: `DELETE /api/options/{id}`
- **URL Parameters**:
  - `id` (required): 选项的唯一标识符。
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**: `{ "message": "Option deleted successfully." }`
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "Option not found." }`



## API 文档 - 问题管理

它适用于 `QuestionController` 类。这个文档清晰地描述了每个API端点的详细信息，包括请求方法、路径、参数及预期的响应。

### 1. 给某个问卷添加问题

- **Endpoint**: `POST /api/surveys/{surveyId}/questions`
- **URL Parameters**:
  - `surveyId` (required): 问卷的唯一标识符。
- **Request Body**: JSON 格式的 `Question` 对象，示例:
  ```json
  {
    "text": "你的年龄是多少？",
    "type": "单选"
  }
  ```
- **Success Response**:
  - **Code**: `201 Created`
  - **Content**:
    ```json
    {
      "id": 1,
      "text": "你的年龄是多少？",
      "type": "单选",
      "surveyId": 1
    }
    ```
- **Error Response**:
  - **Code**: `400 Bad Request`
  - **Content**: `{ "error": "错误信息" }`

### 2. 根据问题ID获取问题

- **Endpoint**: `GET /api/surveys/{surveyId}/questions/{questionId}`
- **URL Parameters**:
  - `surveyId` (required): 问卷的唯一标识符。
  - `questionId` (required): 问题的唯一标识符。
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 1,
      "text": "你的年龄是多少？",
      "type": "单选",
      "surveyId": 1
    }
    ```
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "问题未找到" }`

### 3. 根据问卷ID获取所有问题

- **Endpoint**: `GET /api/surveys/{surveyId}/questions`
- **URL Parameters**:
  - `surveyId` (required): 问卷的唯一标识符。
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    [
      {
        "id": 1,
        "text": "你的年龄是多少？",
        "type": "单选",
        "surveyId": 1
      }
    ]
    ```
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "问卷未找到" }`

### 4. 根据问题ID更新问题

- **Endpoint**: `PUT /api/surveys/{surveyId}/questions/{questionId}`
- **URL Parameters**:
  - `surveyId` (required): 问卷的唯一标识符。
  - `questionId` (required): 问题的唯一标识符。
- **Request Body**: JSON 格式的 `Question` 对象，示例:
  ```json
  {
    "text": "你的职业是什么？",
    "type": "文本"
  }
  ```
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 1,
      "text": "你的职业是什么？",
      "type": "文本",
      "surveyId": 1
    }
    ```
- **Error Response**:
  - **Code**: `400 Bad Request`
  - **Content**: `{ "error": "请求错误" }`

### 5. 根据问题ID删除问题

- **Endpoint**: `DELETE /api/surveys/{surveyId}/questions/{questionId}`
- **URL Parameters**:
  - `surveyId` (required): 问卷的唯一标识符。
  - `questionId` (required): 问题的唯一标识符。
- **Success Response**:
  - **Code**: `204 No Content`
  - **Content**: `{ "message": "问题已成功删除。" }`
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "问题未找到" }`



## API 文档 - 回复管理

适用于 `ResponseController` 类。这个文档详细描述了每个API端点的具体信息，包括请求方法、路径、参数及预期的响应。

### 1. 给某个问题添加回复

- **Endpoint**: `POST /api/responses/{questionId}`
- **URL Parameters**:
  - `questionId` (required): 问题的唯一标识符。
- **Request Body**: JSON 格式的 `ResponseDto` 对象，示例:
  ```json
  {
    "answerText": "26"
  }
  ```
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 1,
      "questionId": 1,
      "answerText": "26"
    }
    ```
- **Error Response**:
  - **Code**: `400 Bad Request`
  - **Content**: `{ "error": "错误信息" }`

### 2. 根据问题ID获取回复

- **Endpoint**: `GET /api/responses/{questionId}`
- **URL Parameters**:
  - `questionId` (required): 问题的唯一标识符。
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    [
      {
        "id": 1,
        "questionId": 1,
        "answerText": "26"
      }
    ]
    ```
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "未找到相关回复" }`

### 3. 根据回复ID删除回复

- **Endpoint**: `DELETE /api/responses/{id}`
- **URL Parameters**:
  - `id` (required): 回复的唯一标识符。
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**: `{ "message": "回复已成功删除。" }`
- **Error Response**:
  - **Code**: `404 Not Found`
  - **Content**: `{ "error": "回复未找到" }`

这是一个使用Markdown格式编写的API文档示例，适用于你的 `SurveyController` 类。这个文档详细描述了每个API端点的具体信息，包括请求方法、路径、参数及预期的响应。

## API 文档 - 问卷管理

- **Data Example**:

```json
{
  "title": "Customer Feedback Survey",
  "description": "A survey to collect customer feedback on our service.",
  "createdBy": 1
}
```

- **Success Response**:
  - **Code**: `200 OK`
  - **Content**: 
    ```json
    {
      "id": 12,
      "title": "Customer Feedback Survey",
      "description": "A survey to collect customer feedback on our service.",
      "createdBy": 1
    }
    ```
- **Error Response**:
  - **Code**: `403 FORBIDDEN`
  - **Content**: `{"error": "You are not authorized to perform this action."}`

### Get All Surveys
- **URL**: `/api/surveys`
- **Method**: `GET`
- **Auth Required**: Yes
- **Permissions**: None (public access)
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**: 
    ```json
    [
      {
        "id": 12,
        "title": "Customer Feedback Survey",
        "description": "A survey to collect customer feedback on our service.",
        "createdBy": 1
      },
      {
        "id": 13,
        "title": "Product Improvement Survey",
        "description": "A survey to understand how we can improve our products.",
        "createdBy": 1
      }
    ]
    ```

### Get a Specific Survey
- **URL**: `/api/surveys/{id}`
- **Method**: `GET`
- **Auth Required**: Yes
- **Permissions**: None (public access)
- **URL Parameters**: `id=[integer]`
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 12,
      "title": "Customer Feedback Survey",
      "description": "A survey to collect customer feedback on our service.",
      "createdBy": 1
    }
    ```

### Update a Survey
- **URL**: `/api/surveys/{id}`
- **Method**: `PUT`
- **Auth Required**: Yes
- **Permissions**: Admin
- **Data Example**:
  ```json
  {
    "title": "Updated Customer Feedback Survey",
    "description": "An updated survey to collect customer feedback more effectively.",
    "createdBy": 1
  }
  ```
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**:
    ```json
    {
      "id": 12,
      "title": "Updated Customer Feedback Survey",
      "description": "An updated survey to collect customer feedback more effectively.",
      "createdBy": 1
    }
    ```

### Delete a Survey
- **URL**: `/api/surveys/{id}`
- **Method**: `DELETE`
- **Auth Required**: Yes
- **Permissions**: Admin
- **Success Response**:
  - **Code**: `200 OK`
  - **Content**: `{"message": "Survey deleted successfully."}`
```

确保前端开发者具有这些API的详细信息，将有助于他们构建与后端服务对接的功能。
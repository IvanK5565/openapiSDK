# DefaultApi

All URIs are relative to *http://localhost:8000/api*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**authorsGet**](#authorsget) | **GET** /authors | Отримати список авторів|
|[**authorsIdDelete**](#authorsiddelete) | **DELETE** /authors/{id} | Видалити автора|
|[**authorsIdGet**](#authorsidget) | **GET** /authors/{id} | Отримати автора за ID|
|[**authorsIdPut**](#authorsidput) | **PUT** /authors/{id} | Оновити дані автора|
|[**authorsPost**](#authorspost) | **POST** /authors | Створити нового автора|
|[**booksGet**](#booksget) | **GET** /books | Отримати список книг|
|[**booksIdDelete**](#booksiddelete) | **DELETE** /books/{id} | Видалити книгу|
|[**booksIdGet**](#booksidget) | **GET** /books/{id} | Отримати книгу за ID|
|[**booksIdPut**](#booksidput) | **PUT** /books/{id} | Оновити книгу|
|[**booksPost**](#bookspost) | **POST** /books | Додати нову книгу|

# **authorsGet**
> Array<Author> authorsGet()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let name: string; //Фільтр за іменем автора (optional) (default to undefined)

const { status, data } = await apiInstance.authorsGet(
    name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **name** | [**string**] | Фільтр за іменем автора | (optional) defaults to undefined|


### Return type

**Array<Author>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Успішна відповідь |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authorsIdDelete**
> authorsIdDelete()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: number; // (default to undefined)

const { status, data } = await apiInstance.authorsIdDelete(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Успішно видалено |  -  |
|**404** | Автор не знайдений |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authorsIdGet**
> Author authorsIdGet()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: number; // (default to undefined)

const { status, data } = await apiInstance.authorsIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**number**] |  | defaults to undefined|


### Return type

**Author**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Успішна відповідь |  -  |
|**404** | Автор не знайдений |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authorsIdPut**
> authorsIdPut(authorInput)


### Example

```typescript
import {
    DefaultApi,
    Configuration,
    AuthorInput
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: number; // (default to undefined)
let authorInput: AuthorInput; //

const { status, data } = await apiInstance.authorsIdPut(
    id,
    authorInput
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **authorInput** | **AuthorInput**|  | |
| **id** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Автор оновлений |  -  |
|**404** | Автор не знайдений |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authorsPost**
> Author authorsPost(authorInput)


### Example

```typescript
import {
    DefaultApi,
    Configuration,
    AuthorInput
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let authorInput: AuthorInput; //

const { status, data } = await apiInstance.authorsPost(
    authorInput
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **authorInput** | **AuthorInput**|  | |


### Return type

**Author**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Автор створений |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **booksGet**
> Array<Book> booksGet()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let authorId: number; //Фільтр за автором (optional) (default to undefined)
let title: string; //Пошук за назвою (optional) (default to undefined)

const { status, data } = await apiInstance.booksGet(
    authorId,
    title
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **authorId** | [**number**] | Фільтр за автором | (optional) defaults to undefined|
| **title** | [**string**] | Пошук за назвою | (optional) defaults to undefined|


### Return type

**Array<Book>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Список книг |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **booksIdDelete**
> booksIdDelete()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: number; // (default to undefined)

const { status, data } = await apiInstance.booksIdDelete(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**204** | Книга видалена |  -  |
|**404** | Книга не знайдена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **booksIdGet**
> Book booksIdGet()


### Example

```typescript
import {
    DefaultApi,
    Configuration
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: number; // (default to undefined)

const { status, data } = await apiInstance.booksIdGet(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**number**] |  | defaults to undefined|


### Return type

**Book**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Книга знайдена |  -  |
|**404** | Книга не знайдена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **booksIdPut**
> booksIdPut(bookInput)


### Example

```typescript
import {
    DefaultApi,
    Configuration,
    BookInput
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let id: number; // (default to undefined)
let bookInput: BookInput; //

const { status, data } = await apiInstance.booksIdPut(
    id,
    bookInput
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bookInput** | **BookInput**|  | |
| **id** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Книга оновлена |  -  |
|**404** | Книга не знайдена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **booksPost**
> Book booksPost(bookInput)


### Example

```typescript
import {
    DefaultApi,
    Configuration,
    BookInput
} from './api';

const configuration = new Configuration();
const apiInstance = new DefaultApi(configuration);

let bookInput: BookInput; //

const { status, data } = await apiInstance.booksPost(
    bookInput
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **bookInput** | **BookInput**|  | |


### Return type

**Book**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Книга створена |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


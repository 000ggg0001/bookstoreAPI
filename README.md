# Content of table

- [API Reference](#api-reference)
- [Demo](#demo)

## API Reference

#### Create user

```http
  POST /Account/v1/User
```

| Object | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userName` | `string` | **Required**. user Name |
| `password` | `string` | **Required**. user password |

#### Authorize account

```http
  POST /Account/v1/Authorized
```

| Object | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userName` | `string` | **Required**. user Name |
| `password` | `string` | **Required**. user password |

#### Generate token

```http
  POST /Account/v1/GenerateToken
```
| Object | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userName` | `string` | **Required**. user Name |
| `password` | `string` | **Required**. user password |

#### Delete user

```http
  DELETE /Account/v1/User/{UUID}
```
| Parameters | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `UserId`    | `string` | **Required**. Valid user ID to delete account |

#### Get account information

```http
  GET /Account/v1/User/{UUID}
```

| Parameters | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `UserId`    | `string` | **Required**. Valid user ID to get account info |

#### Get all books information

```http
  GET /Bookstore/v1/Books
```

| Bearer Token | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Token`    | `string` | **Required**. Valid Bearer token |

#### Add list of books to user account

```http
  POST /Bookstore/v1/Books
```

| Bearer Token | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Token`    | `string` | **Required**. Valid Bearer token |

| Object | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `useId`   | `string` | **Required**. Valid user ID is required |
| `isbn`    | `string` | **Required**. Valid book ISBN to update book |

#### Delete books 

````http
  DELETE /BookStore/v1/Books
````

| Bearer Token | Type     | Description                    |
| :-------- | :------- | :-------------------------------- |
| `Token`    | `string` | **Required**. Valid Bearer token |

| Parameters | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `UserId`    | `string` | **Required**. Valid user ID to delete account |

#### Get information about a book

````https
  GET /BookStore/v1/Book
````

| Bearer Token | Type     | Description                    |
| :-------- | :------- | :-------------------------------- |
| `Token`    | `string` | **Required**. Valid Bearer token |

| Parameters | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `UserId`    | `string` | **Required**. Valid book ISBN to specific book |

#### Delete specific book user has

````http
  DELETE /BookStore/v1/Book
````

| Bearer Token | Type     | Description                    |
| :-------- | :------- | :-------------------------------- |
| `Token`    | `string` | **Required**. Valid Bearer token |

| Object | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `isbn`    | `string` | **Required**. Valid book ISBN to delete book |
| `useId`   | `string` | **Required**. Valid user ID is required |

#### Update one book

```http 
  PUT /BookStore/v1/Books/{ISBN}
```

Authentification Bearer token

| Bearer Token | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `Token`    | `string` | **Required**. Valid Bearer token |

| Parameters | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `isbn`    | `string` | **Required**. Valid book ISBN to update book |

| Object | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `useId`   | `string` | **Required**. Valid user ID is required |
| `isbn`    | `string` | **Required**. Valid book ISBN to update book |
  

## Demo 

- [Docs: BookstoreAPI](https://bookstore.toolsqa.com/swagger)

# createUser()

This operation creates a user.

```javascript
createUser(data): Promise<ResStatus>
```

## Request Syntax{#request-syntax}

```javascript
milvusClient.createUser({
   username: string,
   password: string,
   timeout?: number
 })
```

**PARAMETERS:**

- **username** (*string*) -

    **[REQUIRED]**

    The name of the user to create.

- **password** (*string*) -

    **[REQUIRED]**

    The password of the user to create.

- **timeout** (*number*)  -

    The timeout duration for this operation. 

    Setting this to **None** indicates that this operation timeouts when any response arrives or any error occurs.

**RETURNS** *Promise\<ResStatus>*

This method returns a promise that resolves to a **ResStatus** object.

```javascript
{
    code: number,
    error_code: string | number,
    reason: string
}
```

**PARAMETERS:**

- **code** (*number*) -

    A code that indicates the operation result. It remains **0** if this operation succeeds.

- **error_code** (*string* | *number*) -

    An error code that indicates an occurred error. It remains **Success** if this operation succeeds. 

- **reason** (*string*) - 

    The reason that indicates the reason for the reported error. It remains an empty string if this operation succeeds.

## Example{#example}

```java
milvusClient.createUser({
   username: 'exampleUser',
   password: 'examplePassword',
 })
```


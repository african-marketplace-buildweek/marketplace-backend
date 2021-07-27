# marketplace-backend

## Base URL https://buildweekproject.herokuapp.com

## Auth

### POST (Register)
<details>
    <summary>https://buildweekproject.herokuapp.com/api/auth/register</summary>

    Body Requirements:

    username (string) (required)
    password (string) (required)
    user_picture (string) (optional)

    You will recieve a registered user object.

    Example Result:

    { 
        "user_id": 3,
        "username": "neville",
        "password": "$2a$08$eVblG7WByjvUTGkXnJVQKOD2E9w34DV1I0MDJ9CTlLfkpCu/UOAju"
    }
</details>

### POST (Login)
<details>
    <summary>https://buildweekproject.herokuapp.com/api/auth/login</summary>

    Body Requirements:

    username (string) (required)
    password (string) (required)

    You will recieve a welcome back message with the user's token.

    Example Result:

    {
        "message": "neville is back!",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWJqZWN0IjozLCJ1c2VybmFtZSI6Im5ldmlsbGUiLCJpYXQiOjE2MjczMTgyNzcsImV4cCI6MTYyNzQwNDY3N30.-fR-iAg5RggE9HpWAScdHxlxwknxw7wx0nMxGgQbqpI"
    }
</details>

## Users

### GET

<details>
    <summary>https://buildweekproject.herokuapp.com/api/users</summary>

    You will recieve an array of user objects.

    Example Result:

    [
      { 
        username: 'harry',
        password: '1234',
        user_picture: 'https://upload.wikimedia.org/wikipedia/en/d/d7/Harry_Potter_character_poster.jpg',
        "created_at": "2021-07-25T23:36:57.454Z",
        "updated_at": "2021-07-25T23:36:57.454Z"
      },
      { 
        username: 'hermione',
        password: '1234',
        user_picture: 'https://static.wikia.nocookie.net/characters/images/a/a5/Latest_%2810%29.jpg/revision/latest?cb=20141230074301',
        "created_at": "2021-07-25T23:36:57.454Z",
        "updated_at": "2021-07-25T23:36:57.454Z"
      }
    ]
    
</details>

### POST
<details>
    <summary>https://buildweekproject.herokuapp.com/api/items</summary>

    Body Requirements:

    username (string) (required)
    password (string) (required)
    user_picture (string) (optional)

</details>


## Items

### GET
<details>
    <summary>https://buildweekproject.herokuapp.com/api/items</summary>

    You will recieve an array of item objects.

    Example Result:

    [
        {
            item_id: 1,
            item_name: 'Eggs',
            item_category: 'Animal Products',
            item_price: 2,
            item_description: 'Fresh, organic, cage-free eggs',
        },
        {
            item_id: 2,
            item_name: 'Ham',
            item_category: 'Animal Products',
            item_price: 8.50,
            item_description: 'Fresh, organic, cage-free ham',
        }
    ]

</details>

### POST

<details>
    <summary>https://buildweekproject.herokuapp.com/api/items</summary>

    Body Requirements:

    item_name (string) (required)
    item_category (string) (required)
    item_price (float) (required)
    item_description (string) (required)

</details>

### PUT

### DELETE

## Markets

### GET

## Need some dummy data?

https://buildweekproject.herokuapp.com/api/users/userDummyData
https://buildweekproject.herokuapp.com/api/items/itemDummyData
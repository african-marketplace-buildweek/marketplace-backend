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
    market_id (integer) (required)

    You will recieve a registered user object.

    Example Result:

    { 
        "user_id": 3,
        "username": "neville",
        "password": "$2a$08$eVblG7WByjvUTGkXnJVQKOD2E9w34DV1I0MDJ9CTlLfkpCu/UOAju",
        "market_id": 3
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

### PUT
<details>
    <summary>https://buildweekproject.herokuapp.com/api/users/:id</summary>

    Body Update Options:

    username (string)
    password (string)
    user_picture (string)
    market_id (string)

    You will recieve a an updated user object.

    Example Result:

    {
        "user_id": 2,
        "username": "barry",
        "user_picture": "picture.url",
        "market_id": 1
    }

</details>

### DELETE
<details>
    <summary>https://buildweekproject.herokuapp.com/api/users/:id</summary>

    You will recieve an object containing data from the deleted user.

    Example Result:

    {
        "user_id": 1,
        "username": "harry",
        "password": "1234",
        "user_picture": "https://upload.wikimedia.org/wikipedia/en/d/d7/Harry_Potter_character_poster.jpg",
        "created_at": "2021-07-29T03:14:40.713Z",
        "updated_at": "2021-07-29T03:14:40.713Z",
        "market_id": 1
    }
    
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
### PUT
<details>
    <summary>https://buildweekproject.herokuapp.com/api/items/:id</summary>

    Item Update Options:

    item_name (string)
    item_category (string)
    item_price (float)
    item_description (string)

    You will recieve a an updated item object.

    Example Result:

    {
        "item_id": 2,
        "item_name": "Eggs",
        "item_category": "Animal Products",
        "item_price": 3000,
        "item_description": "Fresh, organic, cage-free eggs"
    }

</details>

### DELETE
### DELETE
<details>
    <summary>https://buildweekproject.herokuapp.com/api/items/:id</summary>

    You will recieve an object containing data from the deleted item.

    Example Result:

    {
        "item_id": 1,
        "item_name": "Eggs",
        "item_category": "Animal Products",
        "item_price": 2,
        "item_description": "Fresh, organic, cage-free eggs"
    }
    
</details>

## Markets

### GET
<details>
    <summary>https://buildweekproject.herokuapp.com/api/markets</summary>

    You will recieve an array of market objects.

    Example Result:

    [
        {
            "market_id": 1,
            "market_name": "South Africa"
        },
        {
            "market_id": 2,
            "market_name": "Middle Africa"
        },
        {
            "market_id": 3,
            "market_name": "East Africa"
        },
        {
            "market_id": 4,
            "market_name": "West Africa"
        },
        {
            "market_id": 5,
            "market_name": "North Africa"
        }
    ]
    
</details>

## Need some dummy data?

https://buildweekproject.herokuapp.com/api/users/userDummyData
https://buildweekproject.herokuapp.com/api/items/itemDummyData

## Market Legend

Each market_id corresponds to a different region in Africa:

1 = South Africa

2 = Middle Africa

3 = East Africa

4 = West Africa

5 = North Africa
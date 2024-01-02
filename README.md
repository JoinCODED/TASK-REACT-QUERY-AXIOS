# 🐶 Pets Form

In this task, you are going to crate a form to add a new pet to the pets website.

## Instructions

- Fork and clone [this repository]() to your `Development` folder.
- Install Axios npm install axios
- Install ReactQuery 
### Axios & ReactQuery Setup
1. In index.js setup ReactQuery Hint (`https://tanstack.com/query/latest/docs/react/installation`)

### Using Axios & ReactQuery to get pets

1. Create a folder called `api` in `src`.
2. Create a file `pets.js`.
3. In `api/pets.js` create a fetchPets function ( make sure to use : async , await)
4. Import the function in `App.js`
5. FetchRooms should be triggered once App is rendered 

### Using Axios add a pet

1. In `api/pets.js` create a createPet function ( make sure to use : async , await )
2. Import the function where you need to create a pet
3. Refresh the page to see the change

### Challenge

1. Do the same steps to update a pet

## here are all the APIs

| Title          | Method   | Endpoint                                                   | Data required           |
| -------------- | -------- | ---------------------------------------------------------- | ----------------------- |
| Fetch all pets | `GET`    | `https://coded-pets-api-crud.eapi.joincoded.com/pets`       |                         |
| Fetch one pet  | `GET`    | `https://coded-pets-api-crud.eapi.joincoded.com/pets/${id}` |                         |
| Create a pet   | `POST`   | `https://coded-pets-api-crud.eapi.joincoded.com/pets`       | `name`, `image`, `type`, `adopted` |
| Delete a pet   | `DELETE` | `https://coded-pets-api-crud.eapi.joincoded.com/pets/${id}` |                         |



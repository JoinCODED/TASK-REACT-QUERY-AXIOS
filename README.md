# 🐶 Pets Form

In this task, you are going to crate a form to add a new pet to the pets website.

## Instructions

- Fork and clone [this repository]() to your `Development` folder.
- Install Axios npm install axios

### Using Axios get pets

1. Create a folder called `api` in `src`.
2. Create a file `pets.js`.
3. In `api/pets.js` create a fetchPets function ( make sure to use : async , await, try and catch )
4. Import the function in `App.js`
5. FetchRooms should be triggered once App is rendered (Hint: 'useEffect')
6. Don't forget to setPets based on the response coming from the API

### Using Axios add a pet

1. In `api/pets.js` create a createPet function ( make sure to use : async , await, try and catch )
2. Import the function where you need to create a pet
3. Refresh the page to see the change

### Challenge

1. Do the same steps to update a pet

## here are all the APIs

| Title          | Method   | Endpoint                                                   | Data required           |
| -------------- | -------- | ---------------------------------------------------------- | ----------------------- |
| Fetch all pets | `GET`    | `https://pets-react-query-backen.herokuapp.com/pets`       |                         |
| Fetch one pet  | `GET`    | `https://pets-react-query-backen.herokuapp.com/pets/${id}` |                         |
| Create a pet   | `POST`   | `https://pets-react-query-backen.herokuapp.com/pets`       | `name`, `image`, `type`, `adopted` |
| Update a pet   | `PUT`    | `https://pets-react-query-backen.herokuapp.com/pets/${id}` | `adopted`               |
| Delete a pet   | `DELETE` | `https://pets-react-query-backen.herokuapp.com/pets/${id}` |                         |

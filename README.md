# Task 1 React Router

- First install react router `npm i react-router-dom`
- Import `BrowserRouter` and wrap it around `<App/>` in `index.js`
- Go to `App.js` and add your `Routes` and `Route` for each page
  - `Home` -> `path='/'`
  - `PetList` -> `path='/pets'`
  - `PetDeital` -> `path='/pets/:petId'`
- Go to `Navbar.js` and edit each `<a>` tag to be `<NavLink>` dont forget to add the `to='pathName'` and remove `href`
- Go to `PetItem.js` and wrap a `<Link>` to the `button` so when you click on it, it taks you to the petDetail page.
  - Dont forget to pass the id of the pet
  - Hint: `<Link to="/pets/${pet.id}"`>
- Go to `PetDetail.js` and get the `petId` from the url using `useParams`
  - Hint: `const {petId} = useParams()`
  - Then try to use the find method on `petsData` to get the correct pet from the list
  - If there is no pet with the same `petId` return `<h1>There is no pet with the id: ${petId}</h1>`

# 🐶 Pets Form

In this task, you are going to crate a form to add a new pet to the pets website.

## Seting up Axios

- install axios using `npm i axios`
- Create a folder called `api` in the `src` directory
- inside this folder create a file called `index.js`
- inside `index.js` import `axios`
- use the bellow table to figure out whats the `baseURL`
- Then create an instance using this `axios.create({baseURL: baseURL})`. refer to the docs for [axios](https://axios-http.com/docs/intro)
- export as default your `instance`
 Hint: 
```js
import axios from "axios";

const instance = axios.create({
  baseURL: "https://pets-react-query-backen.herokuapp.com",
});

export default instance;
```

##  ****Setup React-Query Client****
    
    # **Setup React-Query Client**
    
    ## **Step 1: Install React Query**
    
    First, install React Query using npm. In your terminal, navigate to the project directory and run the following command:
    
    ```
    npm install @tanstack/react-query
    ```
    
    ## **Step 2: Adding Client Provider**
    
    ```
     import { QueryClient, QueryClientProvider} from '@tanstack/react-query'
    
     // Create a client
     const queryClient = new QueryClient()
    
     function App() {
       return (
         // Provide the client to your App
         <QueryClientProvider client={queryClient}>
            // Your Content
         </QueryClientProvider>
       )
     }
    ```

## Creating our first api

- create another file in api called `pets.js`
- inside `pets.js` import the instance you just created
- create a function for each enpoint

  - one for getting all the pets
  - one for getting one pet by ID
  - one for adding a new pet
  - one for updating a pet by ID
  - one for deleting a pet by ID

- In `PetList.js` call the api using useEffect and remove the petsData `Its no longer needed pur data is now coming from the backend.`
- In `PetDetail.js` call the get by id function to get the pet and remove the `petsData`
- In `PetDetail.js` make the update button work
- In `PetDetail.js` make the delete button work
- In `Modal.js` call the api and send the new pet data 

### Challenge

1. Do the same steps to update a pet

## here are all the APIs

| Title          | Method   | Endpoint                                                   | Data required           |
| -------------- | -------- | ---------------------------------------------------------- | ----------------------- |
| Fetch all pets | `GET`    | `https://coded-pets-api-crud.eapi.joincoded.com/pets`       |                         |
| Fetch one pet  | `GET`    | `https://coded-pets-api-crud.eapi.joincoded.com/pets/${id}` |                         |
| Create a pet   | `POST`   | `https://coded-pets-api-crud.eapi.joincoded.com/pets`       | `name`, `image`, `type`, `adopted` |
| Delete a pet   | `DELETE` | `https://coded-pets-api-crud.eapi.joincoded.com/pets/${id}` |                         |



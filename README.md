#Interviewer - Much Better Than The Rest
----------------------------------------

Thank you for taking the time to do this technical test. There are two parts to it:

- [A coding test](#coding-test) - to show off your coding skills and how you do things
- [and a few questions](#questions) - just to find out a bit more about you

Please submit your results as a **zip** file containing **both** the **coding test** in a folder and the **markdown file** with your answers to the questions. Share a private link to this zip file in your Dropbox / Google Drive / OneDrive / wherever.

## Coding Test

### The task

The task is to create an backend application that provides a set of APIs to be called from a frontend UI.

### The API

The API will have 4 endpoints and will communicate JSON with at least the following functionality for each end point:

- `/login` -  a POST request that will accept no input and return a `token` (which need to be used in subsequent calls to the API, in the `Authorization` header). Every call  to `/login` will return a new token and every invocation to this endpoint creates a new user, gives them a preset balance in a preset currency. 
- `/balance` -  a GET request that will accept an `Authorization` header (with the token value output from `/login`) and  will return the current balance along with the currency code.
- `/transactions` - a GET request that will accept an `Authorization` header (with the token value output from `/login`) and  will return a list of transactions done by the user with atleast the `date`, `description`, `amount`, `currency` for each transaction.
- `/spend` - a POST request that will accept an `Authorization` header (with the token value output from `/login`), JSON content representing one spend transaction with the transaction `date`, `description`, `amount`, `currency`.

There is a *Postman* collection at [Interviewer.postman_collection.json](https://github.com/shanmuha/interviewer/blob/master/Interviewer.postman_collection.json) that you can use to test your API implementation.

### Technology stack

- use an netty based async java framework for the server (preferably [ratpack](https://ratpack.io)) and in-memory datastore for the backend (preferably [aerospike](http://www.aerospike.com/))
- the backend will run as a standalone java process + the in-memory datastore process

### Requirements

- Implement the 4 API endpoints
- Feel free to spend as much or as little time on the exercise as you like
- Feel free to use whatever additional frameworks / libraries / packages you like
- Your code should be in a state that you would feel comfortable releasing to production
- Writing unit/integration tests are optional but highly encouraged

# Questions

Please answer the following questions in a markdown file called `answers to questions.md`.

1. How long did you spend on the coding test? What would you add to your solution if you spent more time on it? If you didn't spend much time on the coding test then use this as an opportunity to explain what you would add.
2. What was the most useful feature that was added to Java 8? Please include a snippet of code that shows how you've used it.
3. What is your favourite framework / library / package that you love but couldn't use in the task? What do you like about it so much?
4. What great new thing you learnt about in the past year and what are you looking forward to learn more about over the next year?
5. How would you track down a performance issue in production? Have you ever had to do this? Can you add anything to your implementation to help with this?
6. How would you improve the APIs that you just used?
7. Please describe yourself in JSON format.
8. What is the meaning of life?

####Thanks for your time, hope to hear from you soon!

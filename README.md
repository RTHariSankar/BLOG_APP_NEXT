
HI, So if you are just starting please make sure node is installed on your system.

SO lets start.

-- Clone the Git repository on your vs code or any coding softwares.
-- run npm i
-- create .env file
-- -- add fileds like
      DATABASE_URL=<your-postgresql-url>  // create your own db prisma+postgres or postgresql+prisma in neon 
      JWT_SECRET=<your-secret-key>    
      NEXT_PUBLIC_GRAPHQL_URI=http://localhost:3000/api/graphql   //This will be your port were api is you can view

        To create jwt token you can run below code on any plane node terminal and paste above JWT_SECRET
        const crypto = require('crypto');
        const jwtSecret = crypto.randomBytes(64).toString('hex');
        console.log('JWT_SECRET:', jwtSecret);
-- npx prisma migrate dev //for initialising the db tables
-- npx prisma studio (optional) //To view tables and datas on db
-- npm run seed //To add datas to the db automatically
--npm run dev //To start the server


NOW THE PROJECT WILL RUNNING ON PORT "localhost:3000"
Consider checking the cors url provided while hosting on route.ts file


APIS used are :
--POST      --/api/auth/login--/api/auth/signup     (signup and login)
--GET       --/api/posts                            (To get all the posts)
--PUT       --/api/posts/:id                        (To create post)
--DELETE    --/api/posts/:id	                    (To delete a post)
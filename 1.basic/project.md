  - create a database named `sports`.

  use sports

  - list all databases present in local mongod server.

  show dbs

  - create 3 collections named `cricket`, `football`, `TT` in sports databse.
  - add multiple players in those collections which should have fields like `name`, `age` and `email` and `cost`.

  db.createCollection("cricket")
  db.cricket.insert({name:"sam",age:22,email:"sam@gmail.com",cost:200})

  db.createCollection("football")
  db.football.insert({name:"april",age:23,email:"april@live.com",cost:300})

  db.createCollection("TT")
  db.TT.insert({name:"sunny",age:25,email:"sunny@yahoo.com",cost:289})

  - list all collections in sports database.

  db.getCollectionNames()

  - rename `TT` collection to `tennis`.

  db.TT.renameCollection("tennis")

  - create a capped collection called `khokho` which should have max 3 documents.

  db.createCollection("khokho",{capped:true,size:4096,max:3})

  Try inserting more than 3 and see what happens?
  - check whether a collection is capped or not?
  
  db.khokho.isCapped()

  - drop all documents from `football` collection.

  db.football.drop()

  - delete cricket collection completely.
  
  db.cricket.drop()

  - delete sports database. 

  use sports
  db.dropDatabase()

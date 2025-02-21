<!-- Database Assessment -->
<!-- collection   Assessment1 -->

1. db.Assessment1.insertOne({
name:"Aashis",
age: "22",
task: "code"})
2. db.Assessment1.insertMany([
{name:"Aashis",age:23,task:"code"},
{name:"swornim",age:30,},
  {name:"RRR",},
  {name:"test",age:40, email:"test@gmail.com"}])
3. db.Assessment1.find()
            {
            _id: ObjectId('67b89bd00af994d35d67d603')
            }
            {
            _id: ObjectId('67b89c389db5bffdd5c3eb13'),
            name: 'Aashis',
            age: '22',
            task: 'code'
            }
            {
            _id: ObjectId('67b89cfc9db5bffdd5c3eb14'),
            name: 'Aashis',
            age: 23,
            task: 'code'
            }   
            {
            _id: ObjectId('67b89cfc9db5bffdd5c3eb15'),
            name: 'swornim',
            age: 30
            }
            {
            _id: ObjectId('67b89cfc9db5bffdd5c3eb16'),
            name: 'RRR'
            }
            {
            _id: ObjectId('67b89cfc9db5bffdd5c3eb17'),
            name: 'test',
            age: 40,
            email: 'test@gmail.com'
            }
            {
            _id: ObjectId('67b89cfc9db5bffdd5c3eb17'),
            name: 'test',
            age: 40,
            email: 'test@gmail.com'
            }
4. db.Assessment1.findOne({name: 'test'})
 
            {
        _id: ObjectId('67b89cfc9db5bffdd5c3eb17'),
        name: 'test',
        age: 40,
        email: 'test@gmail.com'
        }
5. db.Assessment1.countDocuments({name: "Aashis"}) ---2
6. db.Assessment1.updateOne({name:'test'}, {$set: {name:"assessment_test1"}})
            {
            _id: ObjectId('67b89cfc9db5bffdd5c3eb17'),
            name: 'assessment_test1',
            age: 40,
            email: 'test@gmail.com'
            }

7. db.Assessment1.updateMany({name:"Aashis"},{$set:{name:"Dangol",age:40,address:"sydney"}})
        {
        acknowledged: true,
        insertedId: null,
        matchedCount: 2,
        modifiedCount: 2,
        upsertedCount: 0
        }
8. db.Assessment1.replaceOne({name:"Dangol"},{name:"task123",class:123})
        {
        acknowledged: true,
        insertedId: null,
        matchedCount: 1,
        modifiedCount: 1,
        upsertedCount: 0
        }
9. db.Assessment1.deleteOne({name:"assessment_test1"})
        {
        acknowledged: true,
        deletedCount: 1
        }
10. db.Assessment1.deleteMany({})
        {
        acknowledged: true,
        deletedCount: 6
        }

<!-- collection Task2 -->

db.createCollection("Task2")
1. db.Task2.insertMany([{name:"Aashis", id:123, email:"aashis@gmail.com"},{name:"Swornim",class:4,id:230},{name:"rrr",email:"aashis@123",task:"code"}])
        {
        acknowledged: true,
        insertedIds: {
            '0': ObjectId('67b8a55f9db5bffdd5c3eb19'),
            '1': ObjectId('67b8a55f9db5bffdd5c3eb1a'),
            '2': ObjectId('67b8a55f9db5bffdd5c3eb1b')
        }
        }
2. db.Task2.insertOne({name:'AAkash',age:40,id:1234,age:"dance"})
    {
    acknowledged: true,
    insertedId: ObjectId('67b8a78a9db5bffdd5c3eb1c')
    }
3. db.Task2.replaceOne({name:'rrr'},{name:'Dangol',address:"lidcombe",age:'60'})
    {
    acknowledged: true,
    insertedId: null,
    matchedCount: 1,
    modifiedCount: 1,
    upsertedCount: 0
    }
4. db.Task2.updateOne({name:'Aashis'},{$set: {name:'Dangol',address:"lidcombe",age:'60'}})
    {
    acknowledged: true,
    insertedId: null,
    matchedCount: 1,
    modifiedCount: 1,
    upsertedCount: 0
    }
5. db.Task2.updateMany({name:'Dangol'},{$set: {name:'Aashis',address:"lidcombe",age:'60'}})
    {
    acknowledged: true,
    insertedId: null,
    matchedCount: 2,
    modifiedCount: 2,
    upsertedCount: 0
    }
6. db.Task2.replaceOne({name:'Aashis'}, {name:'12345',address:"lidcombe",age:'60'})
        {
        acknowledged: true,
        insertedId: null,
        matchedCount: 1,
        modifiedCount: 1,
        upsertedCount: 0
        }
7. db.Task2.find().sort({key: 1}) --- sort in ascending order
8. db.Task2.find().limit(2) --- max 2 data.
9. db.Task2.find().skip(3) ------ will skip first 3.
10. db.Task2.deleteMany({name:"12345"})
        {
        acknowledged: true,
        deletedCount: 3
        }
        <!-- make sollection  -->
db.createCollection("taskk3") 
db.createCollection("product")
db.createCollection("code")
<!-- Result -->
        Assessment1
        code
        product
        Task2
        taskk3
<!-- will rename the collection  -->
db.code.renameCollection("DentedCode")
<!-- delete collection  -->
db.DentedCode.drop()

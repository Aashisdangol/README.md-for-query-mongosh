<!-- Database Assessment -->
<!-- collection   Assessment1 -->
# Assessment Collection 

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
            }**
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

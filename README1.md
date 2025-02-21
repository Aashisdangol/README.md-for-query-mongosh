
<!-- collection Task2 -->
# Task2 collection 
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
# Collections 
### Assessment1
### code
### product
### Task2
### taskk3
<!-- will rename the collection  -->
db.code.renameCollection("DentedCode")
<!-- delete collection  -->
db.DentedCode.drop()

<!-- more nested queries -->
db.product.insertMany([
	{name:"Aashis", id:123, email:"aashis@gmail.com"},
	{name:"Swornim",class:4,id:230},
	{name:"eee",email:"aashis@123",task:"code"},
	{name:"bbb",email:"aashis@123",task:"code"},
	{name:"fff",email:"aashis@123",task:"code"},
	{name:"ddd",email:"aashis@123",task:"code"},
	{name:"ccc",email:"aashis@123",task:"code"},
	{name:"fffg",email:"aashis@123",task:"code"}
])
<!-- sort according to id -->
db.product.find().sort({key:1}).skip(1)

<!-- $and will check the condition  -->
db.product.find({
    $and:[
        {email: "aashis@123"},
        {task: "code"}
    ]
})
<!-- $or will combine conditions one must be true  -->

db.product.find({
    $and:[
            {email: "aashis@123"},
            {task: "code"},
        {$or:[
                {name:"aaa"},
                {name:"Aashis"}
            ]}

        ]   
})
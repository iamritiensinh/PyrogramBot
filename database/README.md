<h2>Cảm ơn vì đã sử dụng tôi 💖. Đây là một số ví dụ về mongo db</h2>

<em>MongoDB là một cơ sở dữ liệu tài liệu với khả năng mở rộng và tính linh hoạt mà bạn muốn với việc truy vấn và lập chỉ mục mà bạn cần</em>

<h3>Tạo một bộ sưu tập được gọi là "users"</h3>
<em>Bạn nên nhập thư viện pymongo và <strong>DATABASE URL</strong></em>
<br><br>

```
import pymongo
from config import Config 

DATABASE_URI = Config.DATABASE_URI
DATABASE_NAME = Config.DATABASE_NAME

myclient = pymongo.MongoClient(DATABASE_URI)
mydb = myclient[DATABASE_NAME]

mycol = mydb["users"]

```

<h3>Chèn vào bộ sưu tập</h3>
<em>Thêm người dùng mới vào "users" database</em>

```

import pymongo
from config import Config 

DATABASE_URI = Config.DATABASE_URI
DATABASE_NAME = Config.DATABASE_NAME

myclient = pymongo.MongoClient(DATABASE_URI)
mydb = myclient[DATABASE_NAME]

mycol = mydb["users"]

mydict = { "name": "John", "userid": "76035" }

x = mycol.insert_one(mydict)

```

<h3>Lọc kết quả</h3>
<em>Tìm người dùng từ "users" database.</em>

```

import pymongo
from config import Config 

DATABASE_URI = Config.DATABASE_URI
DATABASE_NAME = Config.DATABASE_NAME

myclient = pymongo.MongoClient(DATABASE_URI)
mydb = myclient[DATABASE_NAME]

mycol = mydb["users"]

myquery = { "name": "katy" }

mydoc = mycol.find(myquery)

for x in mydoc:
  return x
  
```

<h3>Xóa tài liệu</h3>
<em>Xóa người dùng khỏi "users" database.</em>

```

import pymongo
from config import Config 

DATABASE_URI = Config.DATABASE_URI
DATABASE_NAME = Config.DATABASE_NAME

myclient = pymongo.MongoClient(DATABASE_URI)
mydb = myclient[DATABASE_NAME]

mycol = mydb["users"]

myquery = { "name": "milly" }

mycol.delete_one(myquery) 

```

<h3>Cập nhật bộ sưu tập</h3>
<em>Cập nhật chi tiết người dùng từ "users" database.</em>

```

import pymongo
from config import Config 

DATABASE_URI = Config.DATABASE_URI
DATABASE_NAME = Config.DATABASE_NAME

myclient = pymongo.MongoClient(DATABASE_URI)
mydb = myclient[DATABASE_NAME]

mycol = mydb["users"]

myquery = { "name": "jhon" }
newvalues = { "$set": { "userid": "01335" } }

mycol.update_one(myquery, newvalues)

```

<p>For More Information Visit <a href="https://www.w3schools.com/python/python_mongodb_getstarted.asp">w3schools mongodb lession</a>

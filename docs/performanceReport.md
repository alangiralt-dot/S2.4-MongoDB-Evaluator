1. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({},{ "_id": 0 })`
- ⏱️ **Execution time**: 1 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


2. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({},{ "_id": 0, "restaurant_id": 1, "name": 1 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## 🚨 Performance Issues

### ℹ️ Recommendations
- ‼️ Filtering on unindexed field 'name' - performance may suffer.

### 💡 Suggested Indexes
Consider creating these indexes:
```javascript
db.restaurants.createIndex({ name: 1 });
```


3. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({},{ "_id": 0, "restaurant_id": 1, "name": 1, "borough": 1, "cuisine": 1 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## 🚨 Performance Issues

### ℹ️ Recommendations
- ‼️ Filtering on unindexed field 'borough' - performance may suffer.
- ‼️ Filtering on unindexed field 'cuisine' - performance may suffer.
- ‼️ Filtering on unindexed field 'name' - performance may suffer.

### 💡 Suggested Indexes
Consider creating these indexes:
```javascript
db.restaurants.createIndex({ borough: 1 });
db.restaurants.createIndex({ cuisine: 1 });
db.restaurants.createIndex({ name: 1 });
```


4. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({},{ "_id": 0, "restaurant_id": 1, "name": 1, "borough": 1, "address.zipcode": 1 })`
- ⏱️ **Execution time**: 1 ms
- 📚 **Documents returned**: 664
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_DEFAULT

## 🚨 Performance Issues

### ℹ️ Recommendations
- ‼️ Filtering on unindexed field 'borough' - performance may suffer.
- ‼️ Filtering on unindexed field 'name' - performance may suffer.

### 💡 Suggested Indexes
Consider creating these indexes:
```javascript
db.restaurants.createIndex({ borough: 1 });
db.restaurants.createIndex({ name: 1 });
```


5. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "borough": "Bronx" }, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 54
- 🔍 **Documents examined**: 54
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


6. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "borough": "Bronx" }, { "_id": 0 }).limit(5)`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 5
- 🔍 **Documents examined**: 5
- 🛠️ **Execution stage**: LIMIT

## ✅ No significant issues detected


7. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "borough": "Bronx" }, { "_id": 0 }).skip(5).limit(5)`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 5
- 🔍 **Documents examined**: 5
- 🛠️ **Execution stage**: LIMIT

## ✅ No significant issues detected


8. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "grades.score": { "$gt": 90 } }, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 2
- 🔍 **Documents examined**: 2
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


9. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "grades": { "$elemMatch": { "score": { "$gt": 80, "$lt": 100 } } } }, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 1
- 🔍 **Documents examined**: 1
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


10. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "location.coordinates.0": { "$lt": -95.754168 } }, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 0
- 🔍 **Documents examined**: 664
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


11. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "$and": [ { "cuisine": { "$ne": "American" } }, { "grades.score": { "$gt": 70 } }, { "location.coordinates.0": { "$lt": -65.754168 } } ] }, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 1
- 🔍 **Documents examined**: 3
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


12. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "cuisine": { "$ne": "American" }, "grades.score": { "$gt": 70 }, "location.coordinates.0": { "$lt": -65.754168 }}, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 1
- 🔍 **Documents examined**: 3
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


13. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "cuisine": { "$ne": "American" }, "grades.grade": "A", "borough": { "$ne": "Brooklyn" } }, { "_id": 0 }).sort({ "cuisine": -1})`
- ⏱️ **Execution time**: 3 ms
- 📚 **Documents returned**: 318
- 🔍 **Documents examined**: 403
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


14. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "name": { "$regex": "^Wil" }}, { "_id": 0, "restaurant_id": 1, "name": 1, "borough": 1, "cuisine": 1 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 2
- 🔍 **Documents examined**: 2
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


15. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "name": { "$regex": "ces$" }}, { "_id": 0, "restaurant_id": 1, "name": 1, "borough": 1, "cuisine": 1 })`
- ⏱️ **Execution time**: 1 ms
- 📚 **Documents returned**: 2
- 🔍 **Documents examined**: 2
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


16. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "name": { "$regex": "Reg" }}, { "_id": 0, "restaurant_id": 1, "name": 1, "borough": 1, "cuisine": 1 })`
- ⏱️ **Execution time**: 1 ms
- 📚 **Documents returned**: 4
- 🔍 **Documents examined**: 4
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected


17. ## 📊 Query Performance Report

- 🧪 **Query**: `db.restaurants.find({ "borough": "Bronx", "$or": [ { "cuisine": "American" }, { "cuisine": "Chinese" } ] }, { "_id": 0 })`
- ⏱️ **Execution time**: 0 ms
- 📚 **Documents returned**: 22
- 🔍 **Documents examined**: 54
- 🛠️ **Execution stage**: PROJECTION_SIMPLE

## ✅ No significant issues detected



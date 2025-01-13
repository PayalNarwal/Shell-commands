# MongoDB Shell (mongosh) Commands Cheat Sheet

This document provides a quick reference for basic MongoDB Shell (`mongosh`) commands to help you get started.

---

## 1. **Connecting to MongoDB**
- **Connect to MongoDB:**
  ```bash
  mongosh
  ```
- **Connect to a specific database:**
  ```bash
  mongosh <database_name>
  ```
- **Connect to a remote server:**
  ```bash
  mongosh "mongodb://<host>:<port>/<database>"
  ```

---

## 2. **Database Commands**
- **Show current database:**
  ```javascript
  db
  ```
- **Switch or create a database:**
  ```javascript
  use <database_name>
  ```
- **Show all databases:**
  ```javascript
  show dbs
  ```
- **Drop a database:**
  ```javascript
  db.dropDatabase()
  ```

---

## 3. **Collection Commands**
- **Show all collections:**
  ```javascript
  show collections
  ```
- **Create a collection:**
  ```javascript
  db.createCollection("<collection_name>")
  ```
- **Drop a collection:**
  ```javascript
  db.<collection_name>.drop()
  ```

---

## 4. **CRUD Operations**

### Insert Documents:
- **Insert a single document:**
  ```javascript
  db.<collection_name>.insertOne({ key: "value" })
  ```
- **Insert multiple documents:**
  ```javascript
  db.<collection_name>.insertMany([{ key1: "value1" }, { key2: "value2" }])
  ```

### Query Documents:
- **Find all documents:**
  ```javascript
  db.<collection_name>.find()
  ```
- **Find with a filter:**
  ```javascript
  db.<collection_name>.find({ key: "value" })
  ```
- **Find one document:**
  ```javascript
  db.<collection_name>.findOne({ key: "value" })
  ```

### Update Documents:
- **Update a single document:**
  ```javascript
  db.<collection_name>.updateOne({ key: "value" }, { $set: { key: "new_value" } })
  ```
- **Update multiple documents:**
  ```javascript
  db.<collection_name>.updateMany({ key: "value" }, { $set: { key: "new_value" } })
  ```

### Delete Documents:
- **Delete a single document:**
  ```javascript
  db.<collection_name>.deleteOne({ key: "value" })
  ```
- **Delete multiple documents:**
  ```javascript
  db.<collection_name>.deleteMany({ key: "value" })
  ```

---

## 5. **Indexes**
- **Create an index:**
  ```javascript
  db.<collection_name>.createIndex({ key: 1 }) // 1 for ascending, -1 for descending
  ```
- **Show all indexes:**
  ```javascript
  db.<collection_name>.getIndexes()
  ```

---

## 6. **Aggregation**
- **Perform an aggregation query:**
  ```javascript
  db.<collection_name>.aggregate([
    { $match: { key: "value" } },
    { $group: { _id: "$key", total: { $sum: "$otherKey" } } }
  ])
  ```

---

## 7. **Administrative Commands**
- **Check server status:**
  ```javascript
  db.serverStatus()
  ```
- **Show current operations:**
  ```javascript
  db.currentOp()
  ```

---

## 8. **Utility Commands**
- **Clear the shell screen:**
  ```javascript
  cls
  ```
- **Exit the shell:**
  ```javascript
  exit
  ```

---

Keep this cheat sheet handy for quick reference while working with MongoDB Shell (`mongosh`). Happy coding!

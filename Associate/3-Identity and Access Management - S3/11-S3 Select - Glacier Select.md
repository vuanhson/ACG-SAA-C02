## S3 Select & Glacier Select

### S3 Select
S3 Select enables applications to retrieve only a subset of data from an object by using simple SQL expressions. By using S3 Select to retrieve only the data needed by your application, you can achieve drastic performance increases — in many cases, you can get as much as a 400% improvement.

Let’s assume all your data is stored in S3 in zip files that contain CSV files. Without S3 Select, you would need to download, decompress, and process the entire CSV to get the data you needed. With S3 Select, you can use a simple SQL expression to return only the data from the store you’re interested in instead of retrieving the entire object. This means you’re dealing with an order of magnitude less data, which improves the performance of your underlying applications.

### Glacier Select
Some companies in highly regulated industries — e.g., financial services, healthcare, and others — write data directly to Amazon Glacier to satisfy compliance needs like SEC Rule 17a-4 or HIPAA. Many S3 users have lifecycle policies designed to save on storage costs by moving their data into Glacier when they no longer need to access it on a regular basis.

Glacier Select allows you to run SQL queries against Glacier directly.

### Exam Tips
- Remember that S3 Select is used to retrieve only a subset of data from an object by using simple SQL expressions.
- Get data by rows or columns using simple SQL expressions.
- Save money on data transfer and increase speed.
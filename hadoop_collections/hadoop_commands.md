# List Files
```bash
hdfs dfs -ls /
hdfs dfs -ls /user
```
Like ls in Linux but for HDFS

# Create Directory
```bash
hdfs dfs -mkdir /data
hdfs dfs -mkdir -p /warehouse/raw/sales
```
-p creates parent folders automatically

# Upload File (Local -> HDFS)
```bash
hdfs dfs -put sales.csv /data/
```
Or
```bash
hdfs dfs -copyFromLocal sales.csv /data/
```
Hadoop processing cannot read local files

# Download File (HDFS -> Local)
```bash
hdfs dfs -get /data/sales.csv
```
# Delete file or directory
```bash
hdfs dfs -rm /data/sales.csv
hdfs dfs -rm -r /data
```
# Check Disk Usage
```bash
hdfs dfs -du /data
```
# Change Replication Factor
```bash
hdfs dfs -setrep 2 /data/sales.csv
```
# Count Files and Directories
```bash
hdfs dfs -count /data
```
# Change Permission
```bash
hdfs dfs -chmod 755 /data
```
# Check Hadoop Version
```bash
hadoop version
```
# Check Running Services
```bash
Jps
```
# Cluster Health Report
```bash
hdfs dfsadmin -report
```

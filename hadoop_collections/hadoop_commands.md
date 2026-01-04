# List Files
```bash
hdfs dfs -ls /
hdfs dfs -ls /user
```
Like ls in Linux but for HDFS

# Create Directory
hdfs dfs -mkdir /data
hdfs dfs -mkdir -p /warehouse/raw/sales

-p creates parent folders automatically

# Upload File (Local -> HDFS)
hdfs dfs -put sales.csv /data/

Or
hdfs dfs -copyFromLocal sales.csv /data/

Hadoop processing cannot read local files

# Download File (HDFS -> Local)
hdfs dfs -get /data/sales.csv .

# Delete file or directory
hdfs dfs -rm /data/sales.csv
hdfs dfs -rm -r /data

# Check Disk Usage
hdfs dfs -du /data

# Change Replication Factor
hdfs dfs -setrep 2 /data/sales.csv

# Count Files and Directories
hdfs dfs -count /data

# Change Permission
hdfs dfs -chmod 755 /data

# Check Hadoop Version
hadoop version

# Check Running Services
Jps

# Cluster Health Report
hdfs dfsadmin -report

```[gustavoaco@nodo3 hadoop-0.20-mapreduce]$ HADOOP_USER_NAME=hdfs hdfs dfs -mkdir /user/gustavoaco/precious
[gustavoaco@nodo3 hadoop-0.20-mapreduce]$ HADOOP_USER_NAME=hdfs hdfs dfs -put -l /home/gustavoaco/SEBC.zip /user/gustavoaco/precious
[gustavoaco@nodo3 ~]$ HADOOP_USER_NAME=hdfs hdfs dfsadmin -allowSnapshot /user/gustavoaco/precious
Allowing snaphot on /user/gustavoaco/precious succeeded
[gustavoaco@nodo3 ~]$ HADOOP_USER_NAME=hdfs hdfs dfs -createSnapshot /user/gustavoaco/precious sebc-hdfs-test                                                           Created snapshot /user/gustavoaco/precious/.snapshot/sebc-hdfs-test
Created snapshot /user/gustavoaco/precious/.snapshot/sebc-hdfs-test
 [gustavoaco@nodo3 ~]$ HADOOP_USER_NAME=hdfs hdfs dfs -rm -r  /user/gustavoaco/precious/SEBC.zip
 [gustavoaco@nodo3 ~]$HADOOP_USER_NAME=hdfs hdfs dfs -cp /user/gustavoaco/precious/.snapshot/sebc-hdfs-test/SEBC.zip /user/gustavoaco/precious
 ```


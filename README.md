PySpark installation using PyPI is as follows:
```
pip install pyspark
```
If you want to install extra dependencies for a specific component, you can install it as below:
```
pip install pyspark[sql]
```
For PySpark with/without a specific Hadoop version, you can install it by using PYSPARK_HADOOP_VERSION environment variables as below:
```
PYSPARK_HADOOP_VERSION=2.7 pip install pyspark
```
The default distribution uses Hadoop 3.2 and Hive 2.3. If users specify different versions of Hadoop, the pip installation automatically downloads a different version and use it in PySpark. Downloading it can take a while depending on the network and the mirror chosen. PYSPARK_RELEASE_MIRROR can be set to manually choose the mirror for faster downloading.

PYSPARK_RELEASE_MIRROR=http://mirror.apache-kr.org PYSPARK_HADOOP_VERSION=2.7 pip install
It is recommended to use -v option in pip to track the installation and download status.

PYSPARK_HADOOP_VERSION=2.7 pip install pyspark -v
Supported values in PYSPARK_HADOOP_VERSION are:

without: Spark pre-built with user-provided Apache Hadoop

2.7: Spark pre-built for Apache Hadoop 2.7

3.2: Spark pre-built for Apache Hadoop 3.2 and later (default)

Note that this installation way of PySpark with/without a specific Hadoop version is experimental. It can change or be removed between minor releases.

Using Conda
Conda is an open-source package management and environment management system which is a part of the Anaconda distribution. It is both cross-platform and language agnostic. In practice, Conda can replace both pip and virtualenv.

Create new virtual environment from your terminal as shown below:

```
conda create -n pyspark_env
```
After the virtual environment is created, it should be visible under the list of Conda environments which can be seen using the following command:

conda env list
Now activate the newly created environment with the following command:
```
conda activate pyspark_env
```
You can install pyspark by Using PyPI to install PySpark in the newly created environment, for example as below. It will install PySpark under the new virtual environment pyspark_env created above.

```
pip install pyspark
```
Alternatively, you can install PySpark from Conda itself as below:
```
conda install pyspark
```
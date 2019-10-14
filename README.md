## KafkaFirst
# Spring Boot ve Kafka kullanılarak basit proje hazırlama


* C:\ altında _kafka_ isimli klasör oluşturulur. 
kafka klasörü içerisinde "zookeeper_data" ve "kafka-logs" isimli alt klasörler oluşturulur.

* config/zookeeper.properties dosyası içerisinde dataDir adresine, zookeeper_data adresi verilir.
>dataDir=C:\kafka\zookeeper_data


* config/server.properties dosyası içerisinde, log.dirs satırına, kafka-logs adresi verilir.
>log.dirs=C:\kafka\kafka-logs

* config/server.properties dosyası içerisine şu satırlar da yoksa eklenir.

`` offsets.topic.num.partitions=1
min.insync.replicas=1
default.replication.factor=1 
``

* Kafka server çalıştırmak için, cmd ekranı açılır ve şu script çalıştırılır;
>zookeeper-server-start.bat C:\kafka\config\zookeeper.properties

Şu ekran görüntüsü geldiğinde, Kafka server çalışır durumdadır demektir.

![Screenshot](https://user-images.githubusercontent.com/7340804/66754064-d1e17280-ee9d-11e9-852a-fb30792b95e9.png)


Postman uygulaması ile örnek obje post ederek test ederiz;

``{
	"field1" : "field1",
	"field2" : "field2"
}``

![Screenshot_2](https://user-images.githubusercontent.com/7340804/66754232-33a1dc80-ee9e-11e9-80f6-a61ed23c87f6.png)

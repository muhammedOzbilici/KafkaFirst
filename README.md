## KafkaFirst
# Spring Boot ve Kafka kullanılarak basit proje hazırlama


* C:\ altında _kafka_ isimli klasör oluşturulur. 
kafka klasörü içerisinde "zookeeper_data" ve "kafka-logs" isimli alt klasörler oluşturulur.

* config/zookeeper.properties dosyası içerisinde dataDir adresine, zookeeper_data adresi verilir.
>dataDir=C:\kafka\zookeeper_data


* config/server.properties dosyası içerisinde, log.dirs satırına, kafka-logs adresi verilir.
>log.dirs=C:\kafka\kafka-logs

* config/server.properties dosyası içerisine şu satırlar da yoksa eklenir.
>offsets.topic.num.partitions=1
>min.insync.replicas=1
>default.replication.factor=1

* Kafka server çalıştırmak için, cmd ekranı açılır ve şu script çalıştırılır;
>zookeeper-server-start.bat C:\kafka\config\zookeeper.properties

Şu ekran görüntüsü geldiğinde, Kafka server çalışır durumdadır demektir.

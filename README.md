# SBER-DB-HW1

1)DragonFlyDB: CA.
На оф. сайте https://dragonflydb.io/ указано, что "Dragonfly is architected to scale vertically on a single machine", т.е. база данных работает на одной машине, и следовательно не устойчива к "кластеризации".

2)ScyllaDB: CP.
На оф. сайте https://arenadata.tech/products/arenadata-db/ написано: "Arenadata DB реализована на кластере из множества (от двух до сотен) серверов и равномерно распределяет нагрузку и данные между ним". Также отмечено "Полное соответствие принципам строгой изоляции транзакции (принципы ACID). Одни и те же таблицы могут быть использованы для записи и чтения, без страха потерять данные." Таким образом, это CP бд.

3)ScyllaDB: AP.
Согласно официальной документации, (https://docs.scylladb.com/stable/architecture/architecture-fault-tolerance.html) бд не гарантирует "консистентность" данных:
Scylla chooses availability and partition tolerance over consistency, such that:
It’s impossible to be both consistent and highly available during a network partition;
If we sacrifice consistency, we can be highly available.
Т. о. это AP.

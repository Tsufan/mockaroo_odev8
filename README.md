# mockaroo_odev8
patika.dev veri tabanı tablo işlemleri ödev8

1) test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee(
	id INT PRIMARY KEY,
	name varchar(50) NOT NULL,
	birthday DATE,
	email varchar(100)
);
```
![1](islem_1.jpg)
***
2) Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```
insert into employee (id, name, birthday, email) values (1, 'Adrian Dutteridge', '2020/12/08', 'adutteridge0@live.com');
```
ekleme işlemi
![2](islem_2.jpg)
***
3) Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

![3](islem_3.jpg)

```
UPDATE employee
SET name = 'Update Yapıldı'
WHERE id > 45
RETURNING *;
```
![4](islem_4.jpg)
***
4) Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

![5](islem_5.jpg)
```
DELETE FROM employee
WHERE id > 45;
```
![6](islem_6.jpg)
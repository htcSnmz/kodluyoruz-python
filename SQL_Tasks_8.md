1. test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee(
	id SERIAL PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)	
);
```

2. Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```
insert into employee (name, birthday, email) values ('Maddi', '1992-12-31', 'mletson0@wsj.com');
insert into employee (name, birthday, email) values ('Elmore', '1997-11-06', 'epennycook1@people.com.cn');
insert into employee (name, birthday, email) values ('Vonny', '1997-09-09', 'vscrivenor2@salon.com');
insert into employee (name, birthday, email) values ('Catherine', '1994-01-04', 'cbenediktovich3@gnu.org');
insert into employee (name, birthday, email) values ('Gwenore', '1999-03-26', 'gclifft4@mtv.com');
insert into employee (name, birthday, email) values ('Randy', '1998-12-29', 'rberney5@dailymotion.com');
insert into employee (name, birthday, email) values ('Nikos', '1994-04-16', 'nsheaf6@biglobe.ne.jp');
insert into employee (name, birthday, email) values ('Rebekah', '1994-04-06', 'rfuzzard7@sakura.ne.jp');
insert into employee (name, birthday, email) values ('Cosetta', '2000-03-07', 'cmyner8@simplemachines.org');
insert into employee (name, birthday, email) values ('Brooke', '1997-11-24', 'bskoggings9@pinterest.com');
insert into employee (name, birthday, email) values ('Gardiner', '1998-06-15', 'gsprigina@google.it');
insert into employee (name, birthday, email) values ('Stephanie', '1997-09-11', 'smingardb@hugedomains.com');
insert into employee (name, birthday, email) values ('Lowe', null, null);
insert into employee (name, birthday, email) values ('Bertha', '1992-05-31', 'bpeartd@diigo.com');
insert into employee (name, birthday, email) values ('Clarence', '1999-10-24', 'cwhiteforde@deliciousdays.com');
insert into employee (name, birthday, email) values ('Dale', '1993-04-13', 'dlerohanf@usa.gov');
insert into employee (name, birthday, email) values ('Layton', '1994-08-21', 'lbakerg@latimes.com');
insert into employee (name, birthday, email) values ('Lilla', '1993-10-16', 'ldippleh@state.gov');
insert into employee (name, birthday, email) values ('Hunt', '1996-10-02', 'hbodessoni@japanpost.jp');
insert into employee (name, birthday, email) values ('Clerkclaude', '1999-05-22', 'cprinj@tinyurl.com');
insert into employee (name, birthday, email) values ('Claiborn', '1992-01-23', 'cbeneditek@hp.com');
insert into employee (name, birthday, email) values ('Peyter', '1995-03-12', 'ptreecel@accuweather.com');
insert into employee (name, birthday, email) values ('Cale', '1992-01-25', 'cbrownsellm@jigsy.com');
insert into employee (name, birthday, email) values ('Nanete', '1997-10-26', 'nthickingn@answers.com');
insert into employee (name, birthday, email) values ('Chandra', '1991-10-11', 'cbrogionio@tiny.cc');
insert into employee (name, birthday, email) values ('Granny', '1999-12-26', 'gcastillep@webs.com');
insert into employee (name, birthday, email) values ('Lucky', '1994-01-12', 'logleasaneq@ustream.tv');
insert into employee (name, birthday, email) values ('Cherry', '1996-02-19', 'cpenlingtonr@wix.com');
insert into employee (name, birthday, email) values ('Shaylah', '1998-08-04', 'srabbattss@liveinternet.ru');
insert into employee (name, birthday, email) values ('Roland', '2000-01-13', 'rfitzgilbertt@comcast.net');
insert into employee (name, birthday, email) values ('Collie', null, null);
insert into employee (name, birthday, email) values ('Kathlin', '1996-04-01', 'kkenratv@friendfeed.com');
insert into employee (name, birthday, email) values ('Jerry', '2000-08-18', 'jburburoughw@livejournal.com');
insert into employee (name, birthday, email) values ('Rochell', '1993-02-20', 'rclintonx@odnoklassniki.ru');
insert into employee (name, birthday, email) values ('Julie', '2000-09-20', 'jnorsistery@soup.io');
insert into employee (name, birthday, email) values ('Marcile', '1998-04-03', 'mboyingtonz@printfriendly.com');
insert into employee (name, birthday, email) values ('Benedicto', '1994-11-05', 'blenney10@washington.edu');
insert into employee (name, birthday, email) values ('Jourdan', '2000-02-20', 'jorbon11@ifeng.com');
insert into employee (name, birthday, email) values ('Liva', '1996-11-01', 'llancett12@nature.com');
insert into employee (name, birthday, email) values ('Rosy', '2000-07-28', 'rdoyley13@joomla.org');
insert into employee (name, birthday, email) values ('Claus', '1993-01-23', 'cbendelow14@eventbrite.com');
insert into employee (name, birthday, email) values ('Orazio', '1999-06-24', 'opiner15@cmu.edu');
insert into employee (name, birthday, email) values ('Ailyn', '1998-01-12', 'anoni16@icq.com');
insert into employee (name, birthday, email) values ('Shelley', '1998-01-04', 'smcmanus17@t.co');
insert into employee (name, birthday, email) values ('Harbert', '1995-11-26', 'hpappi18@reuters.com');
insert into employee (name, birthday, email) values ('Sharai', '1999-08-30', 'shurdedge19@hc360.com');
insert into employee (name, birthday, email) values ('Rachael', '1996-02-23', 'rsharman1a@wix.com');
insert into employee (name, birthday, email) values ('Sterling', '1999-01-25', 'sganter1b@technorati.com');
insert into employee (name, birthday, email) values ('Kalinda', '1996-03-08', 'kboxell1c@java.com');
insert into employee (name, birthday, email) values ('Winnie', '1997-04-01', 'wgaddie1d@nih.gov');
```

3. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```
UPDATE employee
SET name = 'Penolope'
WHERE id = 3
RETURNING *;


UPDATE employee
SET email = ''
WHERE email LIKE'%gov'
RETURNING *;
```

4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```
DELETE FROM employee
WHERE name LIKE 'P%';


DELETE FROM employee
WHERE id < 10;


DELETE FROM employee
WHERE name IS NULL
RETURNING *;
```


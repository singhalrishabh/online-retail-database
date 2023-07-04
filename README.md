Online retail application database
create 5 tables : Customers, Items, Bank , Bill, Orders, Item_purchased

create database online_retail; use online_retail;

Create table customer(Cust_id int primary key, Cust_name varchar(5), Gender varchar(6), Age int, Phno int not null, Address varchar(15)); select * from customer; Insert into customer(Cust_id,Cust_name, Gender, Age, Phno,Address) values (1001,"MMMI","Male",21,1234567891,"ENFKDMJDCA"), (1002,"GNBO","Male",57,1234567892,"KNGKJNDHLF"), (1003,"YZTT","Female",30,1234567893,"GMJHGLJLGA"), (1004,"KYUU","Male",21,1234567894,"MGNJDIMBMF"), (1005,"RUIZ","Female",50,1234567895,"AFNHDKEAMD"), (1006,"JLEY","Male",21,1234567896,"MCGCNKGCLH"), (1007,"VDAE","Male",41,1234567897,"DAKAJDMNJE"), (1008,"MORQ","Female",26,1234567898,"NJHBGANHLH"), (1009,"ZIJD","Male",22,1234567899,"AGJMAMIDKC"), (1010,"QFNH","Female",39,1234567900,"IHHFGCAEBG"), (1011,"WLER","Male",28,1234567901,"CIMGDFCHBC"), (1012,"EXET","Male",59,1234567902,"JBIHLGJEIA"), (1013,"LFAE","Female",62,1234567903,"EGCBCEKNKN"), (1014,"OXBJ","Male",29,1234567904,"GMDELFBFGC"), (1015,"OCMM","Female",32,1234567905,"NEBGIMHFGB"), (1016,"YOLY","Male",41,1234567906,"AHIBNFCFJN"), (1017,"SFWJ","Female",22,1234567907,"BCIKFJLBAD"), (1018,"NJKS","Female",23,1234567908,"INGJLHDDMA"), (1019,"FQFB","Female",27,1234567909,"JFBHNJEFEE"), (1020,"EPRZ","Male",23,1234567910,"INIJHLLNLH"), (1021,"HIEU","Male",69,1234567911,"MMDLGJGMMF"), (1022,"ACBS","Male",55,1234567912,"EAJGLKKHLH"), (1023,"VAJG","Male",46,1234567913,"CBMAJMJLJE"), (1024,"KXIZ","Male",18,1234567914,"CCJFKCKIDD"), (1025,"QKSP","Female",23,1234567915,"AKCEHABLIN"), (1026,"TLYZ","Female",60,1234567916,"KJMCCHCMEK"), (1027,"DJIV","Female",20,1234567917,"EKDNJICMEL"), (1028,"CJXH","Male",32,1234567918,"BNDGACGNNJ"), (1029,"KAXQ","Male",54,1234567919,"FHIFLFNGEB"), (1030,"WWRE","Male",27,1234567920,"DNDBMILLDA"), (1031,"DJVB","Male",34,1234567921,"NGBAJLFEKJ"), (1032,"OWTO","Female",21,1234567922,"BAGJDEKDJH"), (1033,"SRDR","Male",27,1234567923,"HBANHKKJCC"), (1034,"XERU","Male",30,1234567924,"BCMFBJCDDF"), (1035,"HTYE","Male",42,1234567925,"JKIJFKLGNI"), (1036,"PMYO","Male",30,1234567926,"IFAMENEHMA"), (1037,"MKXX","Female",35,1234567927,"DCLIELKNIA"), (1038,"UQUK","Male",40,1234567928,"ELFGBICAEE"), (1039,"VCPZ","Male",36,1234567929,"JNNBLFLKLM"), (1040,"OMBV","Female",24,1234567930,"BALAJDEALJ"), (1041,"MUKQ","Female",64,1234567931,"MIILANNFGG"), (1042,"QAKO","Male",42,1234567932,"HBENAIKIME"), (1043,"NOIG","Female",44,1234567933,"AIEDGCFKCA"), (1044,"AULQ","Female",22,1234567934,"ILLLDBKMMG"), (1045,"MHOM","Female",50,1234567935,"JHEIGLKHFI"), (1046,"VTUI","Female",36,1234567936,"ABMGEMNCDC"), (1047,"EMDG","Male",28,1234567937,"LKBBGLIKMK"), (1048,"MNEM","Male",37,1234567938,"DCMMMCIBKK"), (1049,"MZAQ","Male",26,1234567939,"CADNHNDMFC");

create table Items( item_id int primary key, item_name varchar(30), price int, discount int); select * from items; Insert into Items (item_id, item_name, price, discount) values (1111,"Ironbox",250,5), (1112,"bread",10,3), (1113,"Broom",29,4), (1114,"Jam",45,2), (1115,"Mat",30,3), (1116,"Book",20,0), (1117,"Kitchen Set",18,1), (1118,"Stove",344,2), (1119,"Table",1004,3), (1120,"Bag",678,4), (1121,"Towel",234,2), (1122,"Loundry bag",50,23), (1123,"Pen",30,23), (1124,"Pillow",300,4), (1125,"Shampoo1",240,2), (1126,"Shampoo2",230,5), (1127,"Bucket",222,43), (1128,"Mug",120,23), (1129,"Olive oil",120,22), (1130,"Peanut butter",90,12), (1131,"Ketchep",100,15), (1132,"Knife",78,16), (1133,"Ghee",134,0), (1134,"Salt",120,0);

 Create table Bank( Bank_acc_no int primary key, Bank_name varchar(20), Cust_id int, foreign key(Cust_id) references customer(Cust_id)); Insert into Bank (Bank_acc_no, Bank_name, Cust_id) values (1234,"HDFC",1001), (1235,"Andra Bank",1002), (1236,"HDFC",1003), (1237,"HDFC",1004), (1238,"HDFC",1005), (1239,"ICICI",1006), (1240,"Andra Bank",1007), (1241,"HDFC",1008), (1242,"Canara",1009), (1243,"Syndicate",1010), (1244,"Andra Bank",1011), (1245,"Canara",1012), (1246,"Andra Bank",1013), (1247,"ICICI",1014), (1248,"Andra Bank",1015), (1249,"ICICI",1016), (1250,"Canara",1017), (1251,"SBI",1018), (1252,"HDFC",1019), (1253,"Syndicate",1020), (1254,"Syndicate",1021), (1255,"Syndicate",1022), (1256,"HDFC",1023), (1257,"Andra Bank",1024), (1258,"ICICI",1025), (1259,"Andra Bank",1026), (1260,"HDFC",1027), (1261,"SBI",1028), (1262,"Andra Bank",1029), (1263,"ICICI",1030), (1264,"Canara",1031), (1265,"ICICI",1032), (1266,"HDFC",1033), (1267,"ICICI",1034), (1268,"HDFC",1035), (1269,"SBI",1036), (1270,"Canara",1037), (1271,"SBI",1038), (1272,"Syndicate",1039), (1273,"ICICI",1040), (1274,"HDFC",1041), (1275,"Syndicate",1042), (1276,"HDFC",1043), (1277,"HDFC",1044), (1278,"ICICI",1045), (1279,"HDFC",1046), (1280,"SBI",1047), (1281,"Andra Bank",1048), (1282,"SBI",1049);

Create table Bill(Bill_no int primary key, Cust_id int, foreign key(Cust_id) references customer(Cust_id), Bank_acc_no int, foreign key(Bank_acc_no) references Bank(Bank_acc_no)); Insert into Bill(Bill_no, Cust_id, Bank_acc_no) values (3333,1006,1239), (3334,1007,1240), (3335,1008,1241), (3336,1009,1242), (3337,1010,1243), (3338,1011,1244), (3339,1012,1245), (3340,1013,1246), (3341,1014,1247), (3342,1015,1248), (3343,1016,1249), (3344,1017,1250), (3345,1028,1261), (3346,1029,1262), (3347,1030,1263), (3348,1031,1264), (3349,1032,1265), (3350,1033,1266), (3351,1034,1267), (3352,1035,1268), (3353,1036,1269), (3354,1037,1270), (3355,1006,1239), (3356,1007,1240), (3357,1008,1241), (3358,1009,1242), (3359,1010,1243), (3360,1011,1244), (3361,1012,1245), (3362,1013,1246), (3363,1014,1247), (3364,1015,1248), (3365,1016,1249), (3366,1017,1250), (3367,1016,1249), (3368,1017,1250), (3369,1028,1261), (3370,1029,1262), (3371,1030,1263), (3372,1031,1264), (3373,1032,1265), (3374,1033,1266), (3375,1034,1267), (3376,1035,1268), (3377,1036,1269), (3378,1037,1270), (3379,1031,1264), (3380,1032,1265), (3381,1033,1266); show tables;

create table orders(order_no int primary key, order_date varchar(15), cust_id int, foreign key(Cust_id) references customer(Cust_id), bill_no int, foreign key(bill_no) references Bill(bill_no)); insert into orders (order_no, order_date, cust_id, bill_no) values (2222,"01-11-2016",1006,3333), (2223,"02-11-2016",1007,3334), (2224,"03-11-2016",1008,3335), (2225,"03-11-2016",1009,3336), (2226,"04-11-2016",1010,3337), (2227,"04-11-2016",1011,3338), (2228,"05-11-2016",1012,3339), (2229,"07-11-2016",1013,3340), (2230,"08-11-2016",1014,3341), (2231,"08-11-2016",1015,3342), (2232,"09-11-2016",1016,3343), (2233,"09-11-2016",1017,3344), (2234,"09-11-2016",1028,3345), (2235,"09-11-2016",1029,3346), (2236,"09-11-2016",1030,3347), (2237,"10-11-2016",1031,3348), (2238,"10-11-2016",1032,3349), (2239,"10-11-2016",1033,3350), (2240,"11-11-2016",1034,3351), (2241,"12-11-2016",1035,3352), (2242,"12-11-2016",1036,3353), (2243,"24-11-2016",1037,3354), (2244,"24-11-2016",1006,3355), (2245,"24-11-2016",1007,3356), (2246,"25-11-2016",1008,3357), (2247,"25-11-2016",1009,3358), (2248,"26-11-2016",1010,3359), (2249,"26-11-2016",1011,3360), (2250,"26-11-2016",1012,3361), (2251,"26-11-2016",1013,3362), (2252,"26-11-2016",1014,3363), (2253,"26-11-2016",1015,3364), (2254,"27-11-2016",1016,3365), (2255,"20-01-2017",1017,3366), (2256,"20-01-2017",1016,3367), (2257,"21-01-2017",1017,3368), (2258,"21-01-2017",1028,3369), (2259,"21-01-2017",1029,3370), (2260,"22-01-2017",1030,3371), (2261,"23-01-2017",1031,3372), (2262,"23-01-2017",1032,3373), (2263,"23-01-2017",1033,3374), (2264,"24-01-2017",1034,3375), (2265,"24-01-2017",1035,3376), (2266,"29-01-2017",1036,3377), (2267,"29-01-2017",1037,3378), (2268,"31-01-2017",1031,3379), (2269,"01-02-2017",1032,3380), (2270,"02-02-2017",1033,3381);

create table item_purchased(Bill_no int,foreign key(bill_no) references Bill(bill_no), Item_id int,foreign key(item_id) references items(item_id), Price int); insert into item_purchased (Bill_no, Item_id, Price) values (3333,1111,250), (3334,1112,10), (3335,1113,29), (3336,1114,45), (3337,1115,30), (3338,1116,20), (3339,1117,18), (3340,1118,344), (3341,1119,1004), (3342,1111,250), (3343,1112,10), (3344,1113,29), (3345,1114,45), (3346,1115,30), (3347,1116,20), (3348,1117,18), (3349,1118,344), (3350,1119,1004), (3351,1111,250), (3352,1112,10), (3353,1113,29), (3354,1114,45), (3355,1115,30), (3356,1116,20), (3357,1117,18), (3358,1118,344), (3359,1119,1004), (3360,1111,250), (3361,1112,10), (3362,1113,29), (3363,1114,45), (3364,1115,30), (3365,1116,20), (3366,1117,18), (3367,1118,344), (3368,1119,1004), (3369,1111,250), (3370,1112,10), (3371,1113,29), (3372,1114,45), (3373,1115,30), (3374,1116,20), (3375,1117,18), (3376,1118,344), (3377,1119,1004), (3378,1111,250), (3379,1112,10), (3380,1113,29), (3381,1114,45), (3333,1115,30), (3334,1116,20), (3335,1117,18), (3336,1118,344), (3337,1119,1004), (3338,1120,678), (3339,1121,234), (3340,1122,50), (3341,1123,30), (3342,1124,300), (3343,1125,240), (3344,1126,230), (3345,1127,222), (3346,1128,120), (3347,1129,120), (3354,1130,90), (3355,1131,100), (3356,1132,78), (3357,1133,134), (3358,1134,120), (3359,1120,678), (3360,1121,234), (3361,1122,50), (3362,1123,30), (3363,1124,300), (3364,1125,240), (3365,1126,230), (3366,1127,222), (3367,1128,120), (3368,1129,120), (3369,1130,90), (3370,1131,100), (3354,1132,78), (3355,1133,134), (3356,1134,120), (3357,1120,678), (3358,1121,234), (3359,1122,50), (3360,1123,30), (3361,1124,300), (3362,1125,240), (3363,1126,230), (3364,1127,222), (3365,1128,120), (3366,1129,120), (3367,1130,90), (3368,1131,100), (3369,1132,78), (3370,1133,134), (3367,1134,120), (3333,1118,344), (3334,1119,1004), (3335,1111,250), (3336,1112,10), (3337,1113,29), (3338,1114,45), (3339,1115,30), (3340,1116,20), (3341,1117,18), (3342,1118,344), (3343,1119,1004), (3344,1111,250), (3345,1112,10), (3346,1113,29), (3347,1114,45), (3348,1115,30), (3349,1116,20), (3350,1117,18), (3351,1118,344), (3352,1119,1004), (3353,1111,250), (3354,1112,10), (3355,1113,29), (3356,1114,45), (3357,1115,30), (3358,1116,20), (3359,1117,18), (3360,1118,344), (3361,1119,1004), (3362,1118,344), (3363,1119,1004), (3364,1111,250), (3365,1112,10), (3366,1113,29), (3367,1114,45), (3368,1115,30), (3369,1116,20), (3370,1117,18), (3371,1118,344), (3372,1119,1004), (3373,1111,250), (3374,1112,10), (3375,1113,29), (3376,1114,45), (3377,1115,30), (3366,1116,20), (3367,1117,18), (3368,1118,344), (3369,1119,1004), (3370,1111,250), (3371,1112,10), (3372,1113,29), (3373,1114,45), (3374,1115,30), (3375,1116,20), (3376,1117,18), (3374,1118,344), (3375,1119,1004);



use online_retail; 
select * from customer where gender = "Male"; select * from customer where age>25; select * from customer where gender = "Female" and age>30;

#count most sold items select item_id, count(item_id) as count from item_purchased group by item_id order by count desc;

#find the top five names of the item that are sold the most select items.item_id, items.item_name, count(item_purchased.item_id) as count from items,item_purchased where items.Item_id = item_purchased.Item_id group by item_purchased.item_id order by count desc limit 5;

#find which female customer has purchased the most amount of products and her age select bill_no, sum(price) as billamount from item_purchased group by bill_no having bill_no in (select bill_no from bill where Cust_id in (select cust_id from customer where gender="Female")) order by billamount desc; select customer.cust_id, customer.age from customer, bill where customer.cust_id=bill.Cust_id and Bill_no=3359;

#find the products that are sold together

SELECT P1.item_id, P2.item_id, Count(DISTINCT S1.bill_no) as count FROM item_purchased P1 JOIN item_purchased P2 ON P1.item_id > P2.item_id LEFT JOIN item_purchased S1 INNER JOIN item_purchased S2 ON S1.bill_no = S2.bill_no ON S1.item_id = P1.item_id AND S2.item_id = P2.item_id GROUP BY P1.item_id, P2.item_id order by count desc;
find out the item names that is purchased by the customers who are more than 50 years of age

select item_name from items where item_id in (select item_id from item_purchased where bill_no in (select bill_no from bill where cust_id in (select cust_id from customer where age >50)));

#count which bank for more transaction select bank_name, count(bank_name) as count from bank group by Bank_name order by count desc limit 1;

#which month has more transaction select count(substr(orders.order_date,4,2)) as count, substr(orders.order_date,4,2) as months from orders, item_purchased where orders.bill_no=item_purchased.Bill_no group by months order by count desc limit 1;
find how many orders does customer with the cuatomerid 1007 or 1008 does on each month

select orders.cust_id, count(substr(orders.order_date,4,2)) as count, substr(orders.order_date,4,2) as months from orders, item_purchased where orders.bill_no=item_purchased.Bill_no and cust_id= 1035 group by months;
what is the discount got per customer in the month of november or feb or jan

select orders.cust_id, sum(items.discount) as total_discount from orders, items, item_purchased where items.item_id=item_purchased.Item_id and orders.bill_no= item_purchased.Bill_no and substr(orders.order_date,4,2) = 02 group by orders.cust_id;

#Find the total amount perchased by each customers select customer.cust_id, item_purchased.Bill_no, sum(item_purchased.Price) total_price from customer, orders, item_purchased where item_purchased.Bill_no=orders.bill_no and customer.Cust_id=orders.cust_id group by item_purchased.bill_no order by customer.cust_id;
find the item names and bill id purchased by each customers

select orders.cust_id, item_purchased.Bill_no, items.item_name from orders, item_purchased, items where items.item_id=item_purchased.Item_id and orders.bill_no = item_purchased.Bill_no order by orders.cust_id;

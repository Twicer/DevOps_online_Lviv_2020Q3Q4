1. Включення та налаштування ACL, tune2fs	-l	/dev/sda2

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_1_1.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_1_2.PNG)

2. Авторизуємось, як guest і створюємо папку acl_test, надаємо права rwx користувачу utest на папку acl_test, створюємо файл utest.txt та перевіряємо права.

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_2.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_2_1.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_2_2.PNG)

3. Використовуючи ACL дозволяємо лише read користувачу utest для папки acl_test, створити файл prohibited.txt заборонено, виконання команди echo «новый контент»> /tmp/acl_test/utest.txt

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_3_access_denided.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_3_access_denided_2.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_3_access_denided_3.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_3_echo_pass.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_3_echo.PNG)

4. На рівні ACL надано всі дозволи, згідно chmod - все заборонено.

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_4.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_4_new.PNG)

5. Для користувача utest встановлюємо права read для папки acl_test, використовуючи -d для використання спадковості батьківської папки, створюємо файл utest2.txt в папці acl_test 

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_5_guest_tmp.PNG)
![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_5_utest2_create_ok.PNG)

6. Встановлюємо маску с правами read для файлу utest.txt та перевіряємо за допомогою getfacl.

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_6_mask.PNG)

7. Видаляємо всі записи ACL, що відносяться до папки acl_test.

![alt text](https://github.com/boikoserhii/DevOps_online_Lviv_2020Q3Q4/blob/master/m5/task5.6/task5_6_7_del_acl.PNG)

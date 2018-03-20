## Task
Використувати тільки модулі Ансібла 
1. Поставити last Tomcat pack
3. Підкинути кастомні файли конфігів з логінем та паролем ( використати модуль Template ) логін та пароль передати задопомогою ansible.vars
4. ‎рестартнути Томкат сервіс 
5. ‎пепевірити чи він піднявся 
7. ‎Збілдити Мавеном ( поставити правильний шлях до .pom файлу та відповідний goal ) hello_world аплікуху взяти з гіт хабу та збілдити .war артефакт 
8. ‎залити артефакт(application) в Tomcat 
9. ‎перевірити наявність application в браузері за адресою
 localhost:8080/hello_world/
6. ‎якщо все нормально поставити Nginx_proxy який редіректить з localhost:80 на localhost:8080/hello_world/
7. ‎можна підкинути нові файли конфігів в nxinx.conf 
8. ‎перезавантажити сервіс 
9. ‎перевірити чи nginx сервіс працює 
10. ‎в ідеалі при відкриванні в браузері localhost - має першою з'являтися аплікуха з Томкату 

##Commands
* ansible command
ansible -m ping all
ansible -m ping localhost
ansible -m shell -a "whoami" localhost
```

* playbook commands

```bash
ansible-playbook -i inventory playbook.yml
ansible-playbook -i inventory-prod playbook.yml -l db
ansible-playbook -i inventory-test playbook.yml -t apache-install
```

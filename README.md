# ansible_homework2
Запуск стенда из директории /ansible_test
Vagrantfile - "подопытная" ВМ для разворачивания nginx средствами ansible (ip = 192.168.59.157)
inventory - файл инвентори ansible, описаны параметры подключения к ВМ
ansible.cfg - файл конфигурации ansible (пользователь, путь до inventory)
nginx.conf.j2 - файл шаблона конфигурации nginx, содержит переменную nginx_listen_port. Размещается в директории /ansible_test/templates
nginx1.yml - плейбук ansible, инсталлирует EPEL repo, из него устанавливает nginx, переписывает дефолтный /etc/nginx/nginx.conf согласно шаблону ngnix.conf.j2
audit.txt - вывод в консоли при первом запуске плейбука на моем стенде

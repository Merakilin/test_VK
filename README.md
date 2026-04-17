# test_VK
Инструкция по запуску
1. Склонировать репозиторий
2. Перейти в данный репозиторий
3. Установить ansible(если не установлен)
4. Проверка
#в check mode (без реальных изменений)
ansible-playbook -i inventory.yml playbook.yml --check

#Реальный запуск (требует права sudo для установки пакетов)
ansible-playbook -i inventory.yml playbook.yml --ask-become-pass

Запуск только конкретных ролей с тегами
ansible-playbook -i inventory.yml playbook.yml --tags nginx
ansible-playbook -i inventory.yml playbook.yml --tags chrony
ansible-playbook -i inventory.yml playbook.yml --tags postgresql

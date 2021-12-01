Aby uruchomić stack i phpMyAdmin należy wykorzystać polecenie ```docker compose up -d```.

Aby utworzyć testową bazę danych należy wykorzystać polecenie ```docker exec <nazwa_kontenera> mysql --execute="CREATE DATABASE <nazwa_bazy_danych>" --user=<nazwa_uzytkownika> --password=<haslo_uzytkownika>```, w moim przypadku ```docker exec spr02-mysql-1 mysql --execute="CREATE DATABASE test" --user=root --password=password```.

Aby wygenerować plik ilustrujący strukturę projektu należy wykorzystać polecenie ```docker container run --rm -it --name mgraph -v $(pwd):/input pmsipilot/docker-compose-viz render -m image docker-compose.yaml```.
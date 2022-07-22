#Задание в рамках курса 'Тестирование ПО'
## Команды GitBash

 1. Создать папку dir_1
      ```
        mkdir dir_1
      ```
 3. Зайти в папку dir_1
   
      ```
       cd dir_1
      ```
   
 3. Создать папку inner_dir_1
   
      ```
       mkdir inner_dir_1
      ```
   
 4. Посмотреть, где ты находишься
  
      ```
       pwd
      ```
  
 5. Находясь в папке dir_1, создать пустой текстовый файл tf_1.txt
  
      ```
       touch tf_1.txt
      ```
 6. Находясь в папке dir_1, через команду cat создать текстовый файл tf_2.txt со следующими строками:
    - the first 1
    - the second 2
    - the third 3
  
    ```
       cat > tf_2.txt

        the first 1
        the second 2
        the third 3
        
       Ctrl+C
    ```
 7. Зайти в папку inner_dir_1
 
      ```
       cd inner_dir_1
      ```
 
 8. Через cat сделать текстовый файл tf_3.txt  c любыми строками
   
       ```
        cat > tf_3.txt
 
          any line 1
          any line 2
          any line 3
     
        Ctrl+C
       ```
 9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2”
   
       ```
        cat >> tf_3.txt 
        the second 2
        
        Ctrl+C
       ```
   
 10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2”
   
        ```
         cat >> tf_3.txt 
         the sec 2
         
         Ctrl+C
        ```

 11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3”
 
        ```
         cat >> /c/Users/anduser/Desktop/Git/hw_git/Git/GitBush_HW_2/dir_1/tf_2.txt

         the sec 3
         
         Ctrl+C
        ```
   
 12. Через cat добавить в текстовый файл tf_3.txt строку "the SeCoNd 2" 
 
        ```
         cat >> tf_3.txt 
         the SeCoNd 2
         
         Ctrl+C
        ```
    
 13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2”
   
        ```
         cat >> /c/Users/anduser/Desktop/Git/hw_git/Git/GitBush_HW_2/dir_1/tf_2.txt
         the seConD 2
         
         Ctrl+C
        ```
    
 14. Сделать текстовый файл tf_4.txt в котором будет 15 строк.
 
        ```
         cat > tf_4.txt
           1
           2
           3
           4
           5
           6
           7
           8
           9
           10
           11
           12
           13
           14
           15
        ```
 15. Сделать текстовый файл tF_5.txt в котором будет 13 строк.
   
        ```
         cat > tf_5.txt
           1
           2
           3
           4
           5
           6
           7
           8
           9
           10
           11
           12
           13
       ```
 16. Вывести список всех файлов в папке.

       ```
        find -type f
       ```

 17. Выйти из папки inner_dir_1
 
       ```
        cd ..
       ```
   
 18. Вывести содержимое файла tf_3.txt в терминал.
 
       ```
        cat inner_dir_1/tf_3.txt
       ```
    
 19. Найти путь к файлу tf_4.txt

       ```
        realpath tf_4.txt
       ```
    
 20. Отчистить файл tf_4.txt от содержимого без удаления самого файла.
    
       ```
        > ./inner_dir_1/tf_4.txt
       ```
    
 21. Найти путь к файлам у которых есть  “tf” в названии.
   
       ```
        find -name "*tf*"
       ```
    
 22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре.

       ```
        find -iname "*tf*"
       ```
   
 23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке

       ```
        grep -s sec *
       ```
   
 24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке

       ```
        grep -is sec *
       ```
   
 25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке

       ```
        grep -ws sec *
       ```
   
 26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке
  
       ```
        grep -wis sec *
       ```
   
 27. Найти строки в файлах где есть комбинация букв “second” в текущей папке

       ```ЖИЛЕТ С ПОЯСОМ - Жакеты - ЖЕНЩИНЫ | ZARA Российская Федерация
        grep -s second *
       ```
    
 28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке

       ```
        grep -is second *
       ```
     
 29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем
    
       ```
        grep second */
       ```
     
 30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке

       ```
        grep -r -l 'second'
       ```
     
 31. Найти все строки во всех файлах где нет комбинации “second”

       ```
        grep -r -v 'second'
       ```
     
 32. Найти только название и путь к файлам где нет комбинации “second”
    
       ```
        grep -r -v -l 'second'     find -type f | xargs grep -Lr second
       ``` 
   
 33. Вывести в терминал 4 последних строк любого текстового файла
   
       ```
        tail -n4 tf_5.txt
       ```
    
 34. Вывести в терминал 4 первые строки любого текстового файла.
   
       ```
        head -n4 tf_5.txt
       ```
   
 35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым.

       ```
        mkdir inner_dir_2; cat > tf_6.txt
        hello world
       ```
   
 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”

       ```
        grep -lr 'sec' | xargs mv -t inner_dir_1
       ```
   
 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”

       ```
        grep -lr sec | xargs cp -t inner_dir_1
       ```
   
 38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл.

       ```
        grep -rh 'sec' >> tf_new.txt
       ```
   
 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec”

       ```
        grep -rl 'sec' | xargs rm -I
       ```
    
 40. Просто вывести в терминал строку “Good job!!”

       ```
        echo 'Good job!!'
       ```


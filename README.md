lighthouse
=========

This role can install lighthouse

Requirements
------------
                                          i::::::ii                                                
                                         i :::::,,,:                                                
                                         :..,::     ii                                              
                                       i,...,, 1fffttii                                             
                                        ......,i11i 1                                               
                                       i,..... 1ii  tf1i                                            
                                         ,..:::i111tt1ii                                            
                                         ,,,: :iii111i i                                            
                                        ,..,::::       ii i                                         
                                      i ...i:: ::::  .,:::     i                                    
                                      :::,:ftiii   i ..,,,,,,,,:                                    
                                  ::,,,, :,iftLfiit1 ..,:,,,,,,.:i                                  
                               i,,,,,,,,: ,,tGCL1fCGL,,,,,,,,,,,. i                                 
                              i:.,,,,,,,,,,,,LC0CCG0L,,,,,,,,,,... i                                
                              i,..,,,,,,,,,,,:G8LC00t,,,,,,,,,..... i                               
                             i:.,...,,,,,,,,,,i0LL00i,,,,,,,,,......ii                              
                             i,..,......,,,,,,.1LL8G ,,,,,.........., i                             
                              ,,,........,,,,,,,iC0G:,,,,,,,... ......: i                           
                            i:.,,,........,,,,,,.f8C:,.,,,,,........,,., i                          
                             :,,,...........,,,,.,GL,.,,,,,..  : .,,,,,,,:iiiii1i                   
                            i,...,    i    ,,,,,,.:1..,,,,,...:  :..,,,,, ttf1iii                   
                            i,.:i1iiii ::,:,: ,,,,..,,,,,,....:i i :,.,,:ttttftii                   
                             ii1i :ii :,,,:: i  1ttt:,,.......,i   i :,.iLLfttft11i                 
                             iii :ii   ,. tffttt1t1:...........:i    i  :  iiiiiii                  
                            iii :    :  ,i11iiii  ,.,,,,,,,...,, i                                  
                           iii : i:  ,:.: :   ii  :.,,,,,,,,,.,,,i        i                         
                           iii: i :  ::..,.,,::,,:i:.,,,,,,,,,,,, i                                 
                          iii::i :,  i:. .,....,,,: :.,,,,,,,..,,:i                                 
                          i  : i ,    ..,  ::,,  ,,,:..,,,,,,,,,,:i                                 
                         ii : ii::   :..:     :i ,,,:,.,,,,,,,,,,:i                                 
                         ii :  :,    ,..: :  ::i ::   ,.,,,,,,,,,,i                                 
                        ii ::      ::,,::: : ,:i :::::,..,,,,,,,,,i                                 
                       ii :,.    :::,,:,:  : : i :,.......,,,,,,,,i                                 
                      i  ::,.:          :    ::,,...............,,i                                 
                      ii          iii        :..   ..  .......,,,, i                                
                       ii          :::,,:   ::. .... ., .....,,,,,:i                                
                         ii   i:,,......,:::::... .. : ......,,,,,,                                 
                             i:,........,::::, ..  . :i,.......,,,, i                               
                            i ..........,:::,.     . :i:.........., i                   

Role Variables
--------------

Ссылка на git-репозиторий Lighthouse с исходным кодом:
lighthouse_code_src: "https://github.com/VKCOM/lighthouse.git"

Список пакетов, обязательных для работы роли:
lighthouse_packages:
  - git
  - nginx
  
Параметры, определяющие каталог для установки Lighthouse, порт веб-сервера и имя конфигурационного файла nginx:
lighthouse_data_dir: "/lighthouse/"
lighthouse_nginx_port: 8888
lighthouse_nginx_conf: "lighthouse.conf"

Dependencies
------------

Для установки Clickhouse требуется роль ansible-clickhouse: https://github.com/AlexeySetevoi/ansible-clickhouse

Example Playbook
----------------
```yaml
- name: Install Lighthouse
  hosts: lighthouse
  gather_facts: false
  roles:
    - role: lighthouse-role
      tags: lighthouse
```

License
-------

BSD

Author Information
------------------

Andrey Chikin
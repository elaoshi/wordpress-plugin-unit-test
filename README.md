# Purpose

    a starter for applying TDD in wordpress plugin development

# Env

    php 7.3.11 + docker compose + wordpress

# Install phpunit steps:

1. start wordpress docker instance:  `docker compose up -d`

2. setup wordpress by access ` http://localhost ` in your browser

3. open a new terminal and run:  `docker exec -it eric-wp-mt_1 /bin/bash`

4. inside docker instance then run : `sh init.sh`
    
    ps: if you already have bootstrap.php , then replace it

    <img src="https://github.com/elaoshi/wordpress-plugin-unit-test/blob/master/screenshots/replace_files.jpg?raw=true" width="500" />
5. when it finished, run : 
    
    ` cd ./wp-content/plugins/my-test-plugin `
    
6. Assume db ( a new db just for testing ) names wordpress_test_db_2:

    `bin/install-wp-tests.sh wordpress_test_db_2 root 'ChangeMeIfYouWant' mysql`

If finished without error , All Done.

6. Type : `phpunit` to start testing

    <img src="https://github.com/elaoshi/wordpress-plugin-unit-test/blob/master/screenshots/test_success.jpg?raw=true" width="500" />

7. If you have any problem, please contact me : ericlzyu at gmail.com

8. When next time you want to test, run : 

    docker exec -it eric-wp-mt_1 /bin/bash

    source env.sh

    cd ./wp-content/plugins/my-test-plugin

    phpunit


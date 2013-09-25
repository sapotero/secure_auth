#Работа с БД

    CREATE DATABASE `login` ;

    CREATE USER 'user'@'localhost' IDENTIFIED BY 'ee11cbb19052e40b07aac0ca060c23ee';
    GRANT SELECT, INSERT, UPDATE ON `login`.* TO 'user'@'localhost'; 

    CREATE TABLE `login`.`users` (
      `id` INT NOT NULL AUTO_INCREMENT PRIMARY KEY, 
      `username` VARCHAR(30) NOT NULL, 
      `email` VARCHAR(50) NOT NULL, 
      `password` CHAR(128) NOT NULL, 
      `country` VARCHAR(50) NOT NULL, 
      `salt` CHAR(128) NOT NULL
    ) ENGINE = InnoDB  DEFAULT CHARACTER SET utf8 COLLATE utf8_bin;

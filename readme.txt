Para que este proyecto funcione tienes que crear con PHPmyAdmin en tu base de datos SQL o tecnología similar los siguientes comandos: 

create database misc;
GRANT ALL ON misc.* TO 'mike'@'localhost' IDENTIFIED BY 'Michael';
GRANT ALL ON misc.* TO 'mike'@'127.0.0.1' IDENTIFIED BY 'Michael';




//===============VERSION 3 ===================================

PARA LA VERSION 3 DEL CRUD QUE INCLUYE TECNOLOGIAS PHP, SQL, JAVASCRIPT y JQUERY se debe añadir los siguiente comandos SQL en tu base de datos: 

CREATE TABLE Position (
  position_id INTEGER NOT NULL AUTO_INCREMENT,
  profile_id INTEGER,
  rank INTEGER,
  year INTEGER,
  description TEXT,
  PRIMARY KEY(position_id),
  CONSTRAINT position_ibfk_1
    FOREIGN KEY (profile_id)
    REFERENCES Profile (profile_id)
    ON DELETE CASCADE ON UPDATE CASCADE
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

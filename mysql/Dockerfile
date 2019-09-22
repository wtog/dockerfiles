FROM ubuntu:14.04

RUN apt-get -y update
RUN apt-get -y install vim mysql-server 
   
RUN /etc/init.d/mysqld start &&\  
    mysql -e "grant all privileges on *.* to 'root'@'%' identified by 'asdf';"&&\  
    mysql -e "grant all privileges on *.* to 'root'@'localhost' identified by 'asdf';"  
   
EXPOSE 3306  
   
CMD ["/usr/bin/mysqld_safe"]

# jboss-5.1.0.GA debian package
## Download

    wget http://switch.dl.sourceforge.net/project/jboss/JBoss/JBoss-5.1.0.GA/jboss-5.1.0.GA-jdk6.zip

## Unzip archive

    unzip jboss-5.1.0.GA-jdk6.zip
	mv jboss-5.1.0.GA jboss-5.1.0.GA.jdk7-clean1

## Gen debian folder

    cd jboss-5.1.0.GA.jdk7-clean1
	dh_make -e kobrin.artem@gmail.com -n -s -c gpl2
	rm debian/*.ex debian/*.EX

## Replace files in debian folder

    cd ..
	git clone https://github.com/puppetnix/jdk1.7.git debian
	cp debian/* jboss-5.1.0.GA.jdk7-clean1/debian/
	

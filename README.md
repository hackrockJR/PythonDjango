# PythonDjango
Clases

Clase # 1

{

1- install python 3.8.5
2- update pip
3- install visual studio code
4- install linter 


pip freeze //visualiza lo que esta instalado. 


instalar virtualenv

pip install virtualenv

validar la instalacion con el comando>

pip freeze 

crear un entorno virtual 

virtualenv test_env

cd test_env

Activar 

C:\Users\jfrom\Desktop\test_env>.\Scripts\activate

Instalar django

https://github.com/probardjango/Guias


iniciamos un nuevo proyecto 

python .\Scripts\django-admin.py startproject test_project


cd test_project

Ejecutar el servidor

python manage.py runserver

Migration Para comunicar con la base de datos. 

1- cerramos el servidor

2- ejecutamos

python manage.py migrate 


Crear superusuario

verificar la consola de credenciales de administracion
http://127.0.0.1:8000/admin


en CMD> 

python manage.py createsuperuser

//////otro entorno//////////

Desktop  

mkdir pd110 && cd pd110 

virtualenv .

.\Scripts\activate

pip freeze

pip install django

dir

cambiamos el nombre de la subcarpeta pd110 por src

cd src

Guardamos el proyecto en sublimetext

sublimetext
	Project
		Add folder to project
			pd110 
sumblimetext
	save project as 
			pd110
			
	
python .\Scripts\django-admin.py startproject pd110

python manage.py runserver

Migration

1- cerramos el servidor

2- ejecutamos

python manage.py migrate 

3- Creamos cuenta de superusuario

python manage.py createsuperuser

4- Cambiar idioma de administracion django 

	pd110
		src
			pd110
				/* settings.py 
				
				
/////Crear aplicacion /////


cerramos el server 

ctrl +C 

1- Creamos el nombre del app

src>python manage.py startapp boletin

2- Modificar en el settings del proyecto en django 
	
	settings.py	
			Installed_APPS
				'boletin', 
				
///crear modelo ///

guardar objetos y sus atributos

models.py
create your models here:

	class Registrado(models.Model):
    nombre= models.CharField(max_length=100, blank=True, null=True)
    email= models.EmailField()
    timestam= models.DateField(auto_now_add=True, auto_now=False)
    
    def __unicode__(self):
    	return self.email
    
    def __str__(self):
        return self.email
			
- En CMD:

 python manage.py makemigrations
 python manage.py migrate
 
////Crear obejtos en la base de datos ///

- cerramos el servidor 

python manage.py shell 

>>> from boletin.models import Registrado
>>> gente = Registrado.objects.all()
>>> gente
<QuerySet []>
>>>
>>> persona1 = Registrado.objects.create(nombre='Juan', email='jfromero160@hotmail.com')
>>> persona1
<Registrado: jfromero160@hotmail.com>
>>>
>>> gente
<QuerySet [<Registrado: jfromero160@hotmail.com>]>
>>>

- Registar el modelo

proyecto
	pd110
		boletin	
			migrations
				admin.py
					from .models import Registrado

					admin.site.register(Registrado)
					
					
					
					
					
 2-Cerrmas la shell en el cmd 
	>>>quit()
	src>python manage.py runserver


}
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Clase # 2

{


}
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////



















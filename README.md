 git remote add origin https://github.com
>> git branch -M main
>> git push -u origin main
>> https://pythonanywhere.com
>> https://github.com/Nouri426                                 
>> python manage.py makemigrations
>> python manage.py migrate
>> from django.urls import path
>> from . import views
>> urlpatterns = [
>>     path('', views.post_list, name='post_list'),
>> ]
>> from django.shortcut import render
>> from .models import Post
>> def post_list(request):
>> posts = Post.objects.all()
>> return render(request, 'blog/post_list.html', {'posts': posts})
>> <!DOCTYPE html>
>> <html>
>> <head>
>> <title>My Django Site</title>
>> </head>
>> <body>
>> <h1>Hello Django!</h1>
>> </body>
>> </html>
>> pip install gunicorn whitenoise
>> pip freeze > requirements.txt
>> ALLOWED_HOSTS = ['localhost', '127.0.0.1', '.onrender.com']
>> MIDDLEWARE = [
>>     'django.middleware.security.SecurityMiddleware',
>>     'whitenoise.middleware.WhiteNoiseMiddleware',
>> ]
>> STATIC_URL = 'static/'
>> STATIC_ROOT = BASE_DIR / 'staticfiles'
>> git add
>> git commit -m
>> git push origin main
>> *.pyc
>> *~
>> __pycache__/
>> myvenv/
>> db.sqlite3
>> /static/
>> .DS_Store
>> from django.contrib import admin
>> from django.urls import path, include
>> 
>> urlpatterns = [
>>     path('admin/', admin.site.urls),
>>     path('', include('blog.urls')),
>> ]
>> from django.urls import path
>> from . import views
>> 
>> urlpatterns = [
>>     path('', views.post_list, name='post_list'),
>> ]
>> from django.shortcuts import render
>> 
>> def post_list(request):
>>     return render(request, 'blog/post_list.html', {})
>> <!DOCTYPE html>
>> <html>
>>     <head>
>>         <title>Django Girls Blog</title>
>>     </head>
>>     <body>
>>         <header>
>>             <h1><a href="/">Django Girls Blog</a></h1>
>>         </header>
>>         <article>
>>             <p>Published: 28.09.2026</p>
>>             <h2><a href="">My First Post</a></h2>
>>             <p>This is the body content of my very first blog post!</p>
>>         </article>
>>     </body>
>> </html>
>> from django.shortcuts import render
>> from django.utils import timezone
>> from .models import Post
>> 
>> def post_list(request):
>>     posts = Post.objects.filter(published_date__lte=timezone.now()).order_by('published_date')
>>     return render(request, 'blog/post_list.html', {'posts': posts})
>> git add .
>> git commit -m "Complete Django Girls tutorial segments"
>> git branch -M main
>> git remote add origin https://github.com
>> git push -u origin main
>> pip install gunicorn whitenoise
>> pip freeze > requirements.txt
>>  pip install --upgrade pip
>> git add .
>> git commit -m "Complete Django Girls tutorial segments"
>> git branch -M main
>> git remote add origin https://github.com
>> git push -u origin main
>> pip install gunicorn whitenoise
>> pip freeze > requirements.txt
>> pip install -r requirements.txt && python manage.py migrate
>> gunicorn Django_Project.wsgi   
>> 

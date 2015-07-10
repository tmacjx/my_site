#coding:utf-8
from django.conf.urls import patterns, include, url
from django.contrib import admin
from article.views import RSSFeed

urlpatterns = patterns('',
    # Examples:
    # url(r'^$', 'my_site.views.home', name='home'),
    # url(r'^blog/', include('blog.urls')),

    
    url(r'^admin/', include(admin.site.urls)),
  
    url(r'^$','article.views.home',name="home"),#主页
    url(r'^about/$','article.views.about',name="about"),#关于我
    url(r'^message/$','article.views.message',name="message"),#留言
    url(r'^archive/$','article.views.archive',name="archive"),#归档
    url(r'^feed/$', RSSFeed(), name = "RSS"),  #新添加的urlconf, 并将name设置为RSS, 方便在模板中使用
    url(r'^search/$','article.views.blog_search', name = "search"),#按文章标题搜索
    url(r'^article/(?P<year>\d{4})/(?P<month>\d{2})/(?P<day>\d{2})/(?P<id>\d+)/$', 'article.views.detail', name="detail"),#每篇文章 
    url(r'^article/(?P<year>\d{4})/(?P<month>\d{1,2})/$','article.views.archive_month',name="archive_month"),#按月归档
    url(r'^articleClassfi/(?P<classfi>\w+)/$', 'article.views.classfiDetail', name="classfiDetail"),#每个分类页下面的文章
    url(r'^articleTag/(?P<tag>\w+)/$', 'article.views.tagDetail', name="tagDetail"),#每个标签页下面的文章
    
   

   

  
)

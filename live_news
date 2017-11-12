#Google news that keeps updated with the real time news.

from bs4 import BeautifulSoup as soup
from urllib.request import urlopen

def G_news():
	url="https://news.google.com/news/rss?ned=in&hl=en-IN"
	#open the Given URL
	Client=urlopen(url)

	xml_page=Client.read()
	Client.close()

	soup_page=soup(xml_page,"xml")
	news_list=soup_page.findAll("item")
	
	for news in news_list:
			print(news.title.text)
			print(news.link.text)
			print(news.pubDate.text)
			print("="*140)
	n=input()

if __name__ == "__main__":
    G_news()

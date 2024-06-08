import discord
from discord.ext import commands
import requests

intents = discord.Intents.default()
intents.message_content = True
bot = commands.Bot(command_prefix='!', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def selam(ctx):
     await ctx.send('selam çevre kirliliği hakkinda bir kaç bilgi almak istermisin')

@bot.command()
async def evet(ctx):
     await ctx.send('guzel! hangi konu hakkinda bilgi almak istersin?')

@bot.command()
async def hayır(ctx):
     await ctx.send('neden? çevre kirliliği çok önemli')

@bot.command()
async def sukirliliği (ctx):
     await ctx.send('Su kirliliği; göl, nehir, okyanus, deniz ve yeraltı suları gibi su barındıran havzalarda görülen kirliliğe verilen genel addır. Her çeşit su kirliliği, kirliliğin bulunduğu havzanın çevresinde veya içinde yaşayan tüm canlılara zarar verdiği gibi, çeşitli türlerin ve biyolojik toplulukların yok olmasına ortam hazırlar.')

     with open('images/sukirliliği.jpg', 'rb') as f:
         picture = discord.File(f)
     await ctx.send(file = picture)

@bot.command()
async def havakirliliği(ctx):
     await ctx.send('Hava kirliliği, havada bulunan yabancı maddelerin belirli bir oranı aşmasıyla oluşur. Bu yabancı maddelerin artışı, insanların ve diğer tüm canlıların sağlığı üzerinde olumsuz bir etki yaratabilir. Hava kirliliğinden kaynaklanan sağlık sorunlarının başında astım, alerji gibi solunum rahatsızlıkları gelir.')

     with open('images/havakirliliği.jpg', 'rb') as f:
         picture = discord.File(f)
     await ctx.send(file = picture)

@bot.command()
async def toprakkirliliği(ctx):
     await ctx.send('Toprak Kirliliği Nedir? Katı (plastik vb gibi toprakta çözünmeyen maddeler), sıvı (atık yağ gibi çevreyi kirletici maddeler), radyoaktif atık ve diğer kirletici unsurlar tarafından toprağın fiziksel ve kimyasal özelliklerinin bozulmasına toprak kirliliği denilmektedir.')

     with open('images/toprakkirliliği.jpg', 'rb') as f:
         picture = discord.File(f)
     await ctx.send(file = picture)

@bot.command()
async def seskirliliği(ctx):
     await ctx.send('Gürültü kirliliği veya diğer adıyla ses kirliliği, insan veya hayvan yaşamını olumsuz etkileyen, dengesini bozan her türlü insan, hayvan ya da makine kaynaklı ses oluşumudur. Dünya çapında dış mekan gürültüsünün kaynağı esas olarak makineler, ulaşım ve taşıma sistemlerinden kaynaklanır.')

     with open('images/seskirliliği.jpg', 'rb') as f:
         picture = discord.File(f)
     await ctx.send(file = picture)

@bot.command()
async def ışıkkirliliği(ctx):
     await ctx.send('Işık kirliliği, ışığın canlıları rahatsız edecek şekilde yanlış kullanılmasıdır. Yanlış yönde, yanlış miktarda, yanlış yerde, aydınlatılması gerekmeyen yerde ışık kullanımı hem ekonomik kayıp hem de rahatsız edici bir durumdur.')

     with open('images/ışıkkirliliği.jpg', 'rb') as f:
         picture = discord.File(f)
     await ctx.send(file = picture)


bot.run("")

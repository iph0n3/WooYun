需要预安装如下程序 
1、pytesseract （可以pip install pytesseract安装） 
2、Python Imaging Library (PIL) 
3、tesseract-ocr 

原理： 
1、利用tesseract 进行验证码的识别。 

2、post暴力猜解 



问题1.验证码的识别率 
进行了一次处理，从正则里可以看到pattern = '^[a-zA-Z0-9]{4}$' 只取识别为4位的字符，如果不是则重新请求验证码，这个在很大程度上提高了识别率。 


问题2.服务端频率验证 
经过我两天的实验观察，早上会有次数限制，连续两天的下午我尝试了大于1161次的登陆都没有限制，不知道是什么原因，也许是我网络问题 

usage:  wooyun.py users.txt passwords.txt
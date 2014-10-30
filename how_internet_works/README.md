# Bagaimana internet bekerja

> This chapter is inspired by a talk "How the Internet works" by Jessica McKellar (http://web.mit.edu/jesstess/www/).

Kami berani pastikan anda menggunakan internet setiap hari. Tetapi apakah anda tahu apa yang sebenarnya terjadi setelah anda mengetikkan http://djangogirls.org di browser dan tekan 'Enter'?

Hal pertama yang perlu anda mengerti adalah bahwa website hanyalah kumpulan file yang tersimpan di hard disk. Sama halnya dengan video, musik ataupun foto-foto anda. Namun ada satu hal yang berbeda, yaitu file-file tersebut merupakan kode komputer yang disebut dengan HTML.

Jika anda tidak terbiasa dengan pemrograman, mungkin pada awalnya akan sedikit sulit untuk memahami HTML, tetapi web browser anda (seperti Chrome, Safari, Firefox, dll.) sangat menyukainya. Web browser memang didesain untuk mengerti kode-kode ini, memproses dan menampilkannya seperti yang anda inginkan.

Seperti file lainnya, kita perlu tempat untuk menyimpan file HTML ini di hard disk. Untuk di internet, kita menggunakan komputer khusus yang kita sebut *server*. Komputer ini tidak memiliki layar, mouse ataupun keyboard, karena fungsi utamanya adalah untuk menyimpan dan menyajikannya melalui internet/jaringan komputer. Karena itulah komputer itu disebut *server / penyaji* -- karena mereka menyajikan data anda.

Oke, anda pasti ingin tahu internet itu seperti apa bukan?

Kami menggambarkanya buat anda! kira-kira seperti ini:

![Figure 1.1](images/internet_1.png)

Looks like a mess, right? In fact it is a network of connected machines (the above mentioned *servers*). Hundreds of thousands of machines! Many, many kilometers of cables around the world! You can visit a Submarine Cable Map website (http://submarinecablemap.com/) to see how complicated the net is. Here is a screenshot from the website:

![Figure 1.2](images/internet_3.png)

It is fascinating, isn't it? But obviously, it is not possible to have a wire between every machine connected to the Internet. So, to reach a machine (for example the one where http://djangogirls.org is saved) we need to pass a request through many, many different machines.

It looks like this:

![Figure 1.3](images/internet_2.png)

Imagine that when you type http://djangogirls.org, you send a letter that says: "Dear Django Girls, I want to see the djangogirls.org website. Send it to me, please!"

Your letter goes to the post office closest to you. Then it goes to another that is a bit nearer to your addressee, then to another and another till it is delivered at its destination. The only unique thing is that if you send letters (*data packets*) frequently to the same place, each letter might go through totally different post offices (*routers*), depending on how they are distributed in each office.

![Figure 1.4](images/internet_4.png)

Yes, it is as simple as that. You send messages and you expect some response. Of course, instead of paper and pen you use bytes of data, but the idea is the same!

Instead of addresses with a street name, city, zip code and country name, we use IP addresses. Your computer first asks the DNS (Domain Name System) to translate djangogirls.org into an IP address. It works a little bit like old-fashioned phonebooks where you could look for the name of the person you want to contact and find their phone number and address.

When you send a letter, it needs to have certain features to be delivered correctly: an address, stamp etc. You also use a language that the receiver understands, right? The same is with *data packets* you send in order to see a website: you use a protocol called HTTP (Hypertext Transfer Protocol).

So, basically, when you have a website you need to have a *server* (machine) where it lives. The *server* is waiting for any incoming *requests* (letters that ask the server to send your website) and it sends back your website (in another letter).

Since this is a Django tutorial, you will ask what Django does. When you send a response, you don't always want to send the same thing to everybody. It is so much better if your letters are personalized, especially for the person that has just written to you, right? Django helps you with creating these personalized, interesting letters :).

Enough talk, time to create!

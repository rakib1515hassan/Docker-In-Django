## Part#1
    >> docker build --tag python-django .
    >> docker run --publish 8000:8000 python-django



## Part#2
    1) It builds the image
      >> docker-compose build



    2) Docker Compose the image
      >> docker-compose run --rm app myproject startproject core .

    `docker-compose run --rm app django-admin startproject core .` কমান্ডটি ব্যবহৃত হয় Django 
     প্রজেক্ট শুরু করার জন্য, যেখানে Docker এবং Docker Compose ব্যবহার করে একটি নির্দিষ্ট কন্টেইনারে 
     Django অ্যাপ্লিকেশন তৈরি করা হয়।

    এই কমান্ডটি বাংলা ভাষায় বোঝাতে গেলে নিম্নলিখিত পয়েন্টগুলো উল্লেখ করা যেতে পারে:

      i) Docker Compose: Docker Compose একটি টুল, যা একাধিক Docker কন্টেইনারের সাথে সহজে কাজ 
         করার সুযোগ দেয়। এটি YAML ফাইল ব্যবহার করে কন্টেইনার কনফিগারেশন সংরক্ষণ করে এবং একাধিক 
         কন্টেইনার একসাথে চালানোর সুবিধা প্রদান করে।

      ii) docker-compose run: docker-compose run কমান্ডটি ব্যবহার করে একটি নির্দিষ্ট সার্ভিসের জন্য একটি 
        কন্টেইনার তৈরি ও চালানো হয়। এখানে app নামে একটি সার্ভিস নির্দিষ্ট করা হয়েছে।

      iii) --rm: --rm ফ্ল্যাগটি নির্দেশ করে যে, কমান্ডটি চলা শেষে কন্টেইনারটি সরিয়ে ফেলা হবে। অর্থাৎ, 
        এটি একটি অস্থায়ী কন্টেইনার তৈরি করে।

      iv) app: এখানে app হলো Docker Compose ফাইলে নির্ধারিত একটি সার্ভিসের নাম। এই সার্ভিসটি একটি Django 
        অ্যাপ্লিকেশনকে নির্দেশ করে।

      v) django-admin startproject core .: `django-admin startproject` কমান্ডটি ব্যবহার করে একটি নতুন 
        Django প্রজেক্ট শুরু করা হয়। এখানে core হলো প্রজেক্টের নাম এবং . (ডট) নির্দেশ করে যে প্রজেক্ট ফাইলগুলো
        বর্তমান ডিরেক্টরিতে তৈরি হবে।



    3) Now Run the Django Server
        >> docker-compose up

 

1. What is the difference between getElementById, getElementsByClassName, and querySelector/ querySelectorAll?

  getElementById(id) 
  একটি element কে তার unique id দিয়ে খুঁজে বের করে।  
  সবসময় একটি element ফেরত দেয় (কারণ id unique হওয়া উচিত)।  


  getElementsByClassName(className) 
  একই class নামের একাধিক element খুঁজে পায়।  
  এটি একটি HTMLCollection ফেরত দেয় (array-like, কিন্তু array methods নেই)।  
  

  querySelector(cssSelector)  
  CSS selector ব্যবহার করে প্রথম matching element রিটার্ন করে।  

  querySelectorAll(cssSelector)
  CSS selector ব্যবহার করে সব matching element ফেরত দেয়।  
  এটি একটি NodeList দেয় (যার মধ্যে forEach() method কাজ করে)।  
  


  2. How do you create and insert a new element into the DOM?

  নতুন element তৈরি করতে document.createElement() ব্যবহার হয়।  
  তারপর সেটাকে parent element এর মধ্যে append/insert করতে হয়।  


3. What is Event Bubbling and how does it work?

Event bubbling হলো DOM এ event propagate হওয়ার একটি প্রক্রিয়া।
কোনো child element এ event ঘটলে (যেমন button click), event প্রথমে সেই child element এ trigger হয়,
তারপর ধীরে ধীরে তার parent → grandparent → document পর্যন্ত উপরে উঠতে থাকে।


4. What is Event Delegation in JavaScript? Why is it useful?

Event delegation হলো একটি technique যেখানে আমরা parent element এ event listener attach করি 
এবং তার children এর events handle করি।
কারণ event bubbling এর মাধ্যমে event parent পর্যন্ত পৌঁছে যায়।


5. What is the difference between preventDefault() and stopPropagation() methods?

preventDefault():
কোনো element এর default behavior কে বন্ধ করে।

stopPropagation():
Event bubbling/propagation বন্ধ করে দেয়।
মানে child এ event trigger হওয়ার পর parent পর্যন্ত আর propagate হবে না।


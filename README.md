# JavaScript-String-Methods




1. slice(start, end)
    slice() একটি string থেকে নির্দিষ্ট অংশ কেটে নেওয়ার জন্য ব্যবহৃত হয়।
    এটি দুটি প্যারামিটার নেয়:
    -start → কোন index থেকে শুরু করবে
    -end → কোন index পর্যন্ত নিবে

Note: যদি একটি প্যারামিটার ব্যাবহার করা হয় সেটি হবে start index.
      Negative index ব্যবহার করলে string এর শেষ থেকে count করা হয়।

Example:

    const text = "JavaScript";
    console.log(text.slice(0, 4)); // "Java"

Explanation:
    এখানে start = 0, end = 4 → index 0 থেকে 3 পর্যন্ত character কেটে নেয়
    output হবে "Java"


2. substring(start, end)
    substring() অনেকটা slice() এর মতোই, তবে এটি নেগেটিভ ইনডেক্স সাপোর্ট করে না (নেগেটিভ দিলে সেটাকে 0 ধরে নেয়)।

    -start → শুরুর ইনডেক্স।
    -end → শেষের ইনডেক্স (এটি ইনক্লুড করা হয় না)।

Example:

    const text = "JavaScript";
    console.log(text.substring(4, 10)); // "Script"

Explanation: 
    ৪ নম্বর ইনডেক্স থেকে শুরু করে ১০ নম্বরের আগ পর্যন্ত অংশটি দেখাবে।


3. replace(searchValue, newValue)
    একটি নির্দিষ্ট শব্দ বা অংশকে অন্য কিছু দিয়ে পরিবর্তন করতে এটি ব্যবহৃত হয়।

    -searchValue → যাকে পরিবর্তন করতে চান।
    -newValue → যা বসাতে চান।

Example:

    const text = "I love Java";
    console.log(text.replace("Java", "JS")); // "I love JS"

Explanation: 
    এখানে "Java" খুঁজে বের করে সেটির জায়গায় "JS" বসিয়ে দেওয়া হয়েছে।


4. toUpperCase() এবং toLowerCase()
    স্ট্রিংয়ের অক্ষরগুলোকে বড় হাতের বা ছোট হাতের করার জন্য ব্যবহৃত হয়।

Example:

    const text = "Hello World";
    console.log(text.toUpperCase()); // "HELLO WORLD"
    console.log(text.toLowerCase()); // "hello world"
    

5. trim()
    স্ট্রিংয়ের শুরুতে এবং শেষে যদি বাড়তি কোনো খালি জায়গা (whitespace) থাকে, তবে তা সরিয়ে ফেলে।

Example:

    const text = "   Hello   ";
    console.log(text.trim()); // "Hello"

6. charAt(index)
    একটি নির্দিষ্ট ইনডেক্স বা অবস্থানে কোন অক্ষরটি আছে তা জানার জন্য এটি ব্যবহৃত হয়।

Example:

    const text = "React";
    console.log(text.charAt(0)); // "R"


7. split(separator)
    কোনো নির্দিষ্ট চিহ্নের ওপর ভিত্তি করে স্ট্রিংকে টুকরো টুকরো করে একটি Array-তে রূপান্তর করে।

Example:

    const text = "apple,banana,mango";
    const fruits = text.split(","); 
    console.log(fruits); // ["apple", "banana", "mango"]
    
8. includes(searchString)
    একটি স্ট্রিংয়ের ভেতর নির্দিষ্ট কোনো শব্দ আছে কি না তা পরীক্ষা করে। এটি true অথবা false রিটার্ন করে।

Example:

    const text = "Learning JavaScript is fun";
    console.log(text.includes("JavaScript")); // true

9. concat()
    দুই বা ততোধিক স্ট্রিংকে একত্রে জোড়া দেওয়ার জন্য ব্যবহৃত হয়।

Example:

    const hello = "Hello";
    const world = "World";
    console.log(hello.concat(" ", world)); // "Hello World"


10. padStart(targetLength, padString) এবং padEnd()
    একটি স্ট্রিং নির্দিষ্ট দৈর্ঘ্যে পৌঁছানোর আগ পর্যন্ত তার শুরুতে বা শেষে অন্য কোনো ক্যারেক্টার যোগ করতে এটি ব্যবহৃত হয়।

    -targetLength → স্ট্রিংটি মোট কত বড় হবে।
    -padString → যা দিয়ে খালি জায়গা পূরণ করবেন।

Example:

    const accountNo = "5432";
    console.log(accountNo.padStart(8, "*")); // "****5432"
    console.log(accountNo.padEnd(8, "0"));   // "54320000"

11. startsWith(searchString) এবং endsWith()
    একটি স্ট্রিং নির্দিষ্ট কোনো শব্দ বা অক্ষর দিয়ে শুরু বা শেষ হয়েছে কি না তা পরীক্ষা করে। এটি true/false রিটার্ন করে।

Example:

    const text = "Hello Developers";
    console.log(text.startsWith("Hello")); // true
    console.log(text.endsWith("World"));   // false

12. indexOf(searchValue) এবং lastIndexOf()
    স্ট্রিংয়ের ভেতর কোনো শব্দের প্রথম (বা শেষ) অবস্থান অর্থাৎ ইনডেক্স খুঁজে বের করার জন্য ব্যবহৃত হয়। না পাওয়া গেলে -1 রিটার্ন করে।

Example:

    const text = "Coding is fun and coding is life";
    console.log(text.indexOf("coding"));     // 18
    console.log(text.lastIndexOf("coding")); // 18 (Case sensitive)


13. repeat(count)
    একটি স্ট্রিংকে নির্দিষ্ট সংখ্যক বার কপি বা রিপিট করার জন্য এটি ব্যবহৃত হয়।

Example:

    const text = "Hello! ";
    console.log(text.repeat(3)); // "Hello! Hello! Hello! "

14. replaceAll(searchValue, newValue)
    replace() শুধু প্রথম ম্যাচটি পরিবর্তন করে, কিন্তু replaceAll() স্ট্রিংয়ের ভেতরে থাকা সবগুলা ম্যাচিং শব্দ পরিবর্তন করে দেয়।

Example:

    const text = "Cats are cute. Cats are fast.";
    console.log(text.replaceAll("Cats", "Dogs")); // "Dogs are cute. Dogs are fast."

15. charCodeAt(index)
    নির্দিষ্ট ইনডেক্সে থাকা অক্ষরের Unicode (ASCII) ভ্যালু জানতে এটি ব্যবহৃত হয়।

Example:

    const text = "ABC";
    console.log(text.charCodeAt(0)); // 65 (A এর ইউনিকোড)


16. match(regexp)
    এটি একটি স্ট্রিংয়ের ভেতর নির্দিষ্ট কোনো Regular Expression বা শব্দ খুঁজে বের করে এবং ফলাফলটি একটি Array হিসেবে রিটার্ন করে।

Example:

    const text = "The rain in SPAIN stays mainly in the plain";
    const res = text.match(/ain/g); 
    console.log(res); // ["ain", "ain", "ain"]

Explanation: 
    এখানে /ain/g দিয়ে পুরো স্ট্রিংয়ে যতবার "ain" আছে তা খুঁজে বের করা হয়েছে।

17. search(searchValue)
    এটি একটি স্ট্রিংয়ের ভেতর নির্দিষ্ট কোনো শব্দ বা Regular Expression সার্চ করে এবং তার প্রথম ইনডেক্স রিটার্ন করে। indexOf() এর মতো হলেও এটি রেগুলার এক্সপ্রেশন সাপোর্ট করে।

Example:

    const text = "Mr. Blue has a blue house";
    console.log(text.search("blue")); // 15


17. localeCompare(compareString)
    দুটি স্ট্রিং একই কি না বা তাদের ক্রম (Alphabetical order) তুলনা করার জন্য এটি ব্যবহৃত হয়। এটি মূলত সর্টিং (Sorting) করার সময় কাজে লাগে।

Example:

    const a = "apple";
    const b = "banana";
    console.log(a.localeCompare(b)); // -1 (কারণ apple ডিকশনারিতে আগে আসে)


19. trimStart() এবং trimEnd()
    আমরা trim() মেথড দিয়ে দুই পাশের স্পেস কেটে দিই, কিন্তু এই মেথডগুলো দিয়ে আপনি চাইলে শুধুমাত্র শুরুতে বা শুধুমাত্র শেষে স্পেস কাটতে পারেন।

Example:

    const text = "   Hello   ";
    console.log(text.trimStart()); // "Hello   "
    console.log(text.trimEnd());   // "   Hello"


20. at(index)
    এটি charAt() এর মতোই, তবে এর স্পেশালিটি হলো এটি Negative index সাপোর্ট করে। অর্থাৎ আপনি চাইলে স্ট্রিংয়ের শেষ থেকে ক্যারেক্টার নিতে পারেন।

Example:

    const text = "JavaScript";
    console.log(text.at(-1)); // "t"
    console.log(text.at(-2)); // "p"


21. slice() vs substring() vs substr()
    আমরা slice() এবং substring() দেখেছি। আগে substr() নামে আরেকটি মেথড ছিল, যা বর্তমানে deprecated (বর্জনীয়) হলেও অনেক পুরনো কোডে দেখা যায়।

    -substr(start, length) -> এটি শুরু থেকে কয়টি ক্যারেক্টার নিবে সেই সংখ্যা (length) অনুযায়ী কাটে।

Example:

    const text = "JavaScript";
    console.log(text.substr(4, 3)); // "Scr"


22. matchAll(regexp)
    match() মেথডটি সব ম্যাচ দিলেও বিস্তারিত তথ্য দেয় না। matchAll() একটি ইটারেটর (Iterator) রিটার্ন করে যেখানে প্রতিটি ম্যাচের ইনডেক্স, গ্রুপসহ বিস্তারিত তথ্য থাকে।

Example:

    const text = "test1, test2";
    const matches = text.matchAll(/test(\d)/g);
    for (const match of matches) {
    console.log(match);
    }


23. valueOf() এবং toString()
    জাভাস্ক্রিপ্টে স্ট্রিং অবজেক্টকে আদি (primitive) স্ট্রিং ভ্যালুতে রূপান্তর করতে এগুলো ব্যবহৃত হয়। সাধারণত জাভাস্ক্রিপ্ট নিজে থেকেই এটি করে নেয়, তাই আলাদা করে লিখতে হয় না।

Example:

    let text = new String("Hello");
    console.log(text.valueOf()); // "Hello"


24. normalize()
    ইউনিকোড ক্যারেক্টারগুলোকে একটি নির্দিষ্ট স্ট্যান্ডার্ড ফরম্যাটে আনার জন্য এটি ব্যবহৃত হয়। বিশেষ করে ইউরোপীয় বা অন্যান্য ভাষার বিশেষ চিহ্ন যুক্ত অক্ষরের ক্ষেত্রে এটি কাজে লাগে।

Note: 
মনে রাখবেন, স্ট্রিং হলো Immutable (অপরিবর্তনশীল)। অর্থাৎ, এই মেথডগুলো ব্যবহার করলে মূল স্ট্রিং পরিবর্তন হয় না, বরং একটি নতুন স্ট্রিং তৈরি হয়।

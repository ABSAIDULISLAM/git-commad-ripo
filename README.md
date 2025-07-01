✅ 1. Project Clone করা
git clone https://github.com/username/project-name.git
cd project-name


✅ 2. Dependencies Install করা
Laravel এর dependency গুলো install করতে হবে:
composer install

✅ 3. .env ফাইল সেটআপ
cp .env.example .env

4. Application Key Generate করা
php artisan key:generate

✅ 5. Database Configuration করা
.env ফাইল ওপেন করে নিচের অংশে আপনার ডেটাবেজ তথ্য বসান:

DB_DATABASE=your_db_name
DB_USERNAME=your_db_user
DB_PASSWORD=your_db_password

✅ 6. Migration & Seeder চালানো (যদি প্রযোজ্য হয়)
php artisan migrate
# অথবা যদি seed data থাকে:
php artisan migrate --seed

 7. Storage Link তৈরি করা (যদি প্রজেক্টে ফাইল/ইমেজ থাকে)
php artisan storage:link

✅ 8. npm install ও assets build করা (যদি frontend compiled হয়)
npm install
npm run dev
# অথবা production mode এ:
npm run build

✅ 9. Server চালানো
php artisan serve
এরপর ব্রাউজারে যান: http://127.0.0.1:8000

অতিরিক্ত টিপস:
যদি Laravel এর ভার্সন match না হয়, তাহলে composer.json দেখে সঠিক PHP/Laravel version ব্যবহার করুন।

.env তে cache সমস্যা হলে:

php artisan config:cache
php artisan route:clear
php artisan view:clear

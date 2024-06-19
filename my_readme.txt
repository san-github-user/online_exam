For Admin template use the following link
https://www.egrappler.com/responsive-bootstrap-admin-template-edmin/

For sepearting layout
view>backend>layout>dashboard,navbar, footer, sidebar, master 

Models-
Quiz
Question
Answer
Result
In last,
php artisan make:migration create_quiz_user_table --create=quiz_user

Fields of quizzes table
string('name')
text('description')
integer('minutes')

Fields of questions
string('question')
integer('quiz_id')

Fields of answers table
integer('question_id')
string('answer')
boolean('is_correct')

Fields of results table
integer('user_id')
interger('question_id')
integer('quiz_id')
integer('answer_id')

Fields of users table
string('visible_password')
string('occupation')->nullable()
string('address')->nullable()
string('phone')->nullable()
integer('is_admin')->default(0)

Fields of quiz_user table
integer('quiz_id')
integer('user_id')

Making Fillable array and Relationship between models

User Model fillable -
name, email, password, visible_password, occupation, address, phone, bio, is_admin

Quiz fillable
name, description, minutes

Question fillable
question, quiz_id

Answer fillable
question_id, answer, is_correct

Result fillable
user_id, question_id, answer_id, quiz_id
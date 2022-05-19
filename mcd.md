CATEGORY: id, name
BELONGS TO, 11 BOOK, 1N CATEGORY: category_id
USER: id, name, email, password

IS WRITTEN BY, 11 BOOK, 1N AUTHOR: author_id
BOOK: id, isbn, title, author, price, years, picture, résumé, editor, category, nb_pages, format
MAKE A, ON REVIEW, 0N USER: user_id

AUTHOR:id, name
HAS, 0N BOOK, 11 REVIEW: review_id
REVIEW:id, comment, created_at, rating
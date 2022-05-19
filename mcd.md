USER: Email, Name, Password, Role, Address
MAKE A, 11 REVIEW, 0N USER
REVIEW: ReviewIdentifier, Comment, PublicationDate, Rating

BELONGS TO, 11 BOOK, 1N CATEGORY
BOOK: ISBN, Title, Author, Price, Years, Picture, Summary, Editor, Category, NumberPages, Format, Status
HAS, 0N BOOK, 11 REVIEW

CATEGORY: CategoryIdentifier, Name
IS WRITTEN BY, 1N BOOK, 1N AUTHOR
AUTHOR: AuthorIdentifier, Name
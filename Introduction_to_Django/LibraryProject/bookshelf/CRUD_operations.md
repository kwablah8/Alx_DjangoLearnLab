#Create a Book Instance

```python
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)
book
```

**Expected Output:**

```python
<Book: 1984 by George Orwell (1949)>
```

---

#Retrieve the Book Instance

```python
from bookshelf.models import Book
book = Book.objects.get(title="1984")
book.title, book.author, book.publication_year
```

**Expected Output:**

```python
('1984', 'George Orwell', 1949)
```

---

#Update the Book Title

```python
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()
book
```

**Expected Output:**

```python
<Book: Nineteen Eighty-Four by George Orwell (1949)>
```

---

#Delete the Book

```python
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()
Book.objects.all()
```

**Expected Output:**

```python
<QuerySet []>  # Book deleted, queryset is now empty
```

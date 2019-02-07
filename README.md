# Try-and-Except

def change_read():
    book_id = ui.get_book_id()
    try:                               #Try statement will search the store to get the book name by its book_id
        book = store.get_book(book_id)
    except:                            # If book is not found or the book_id is incorrect etc, then the 'except' block will be executed
        ui.message('The book is not in Store!')
    else:                              #else as the book name will be retrieved from the store
                                       #it will be certain that the book exists, hence the book_read_value() will be retrieved.
        new_read = ui.get_read_value()
        store.set_book_read(book_id, new_read)

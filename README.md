# artclass Film:
    def __init__(self, title, director, year, genre, duration):
        self.title = title
        self.director = director
        self.year = year
        self.genre = genre
        self.duration = duration
        self.is_watched = False

    def watch(self):
        if not self.is_watched:
            self.is_watched = True
            print(f"You are now watching '{self.title}' directed by {self.director}. Enjoy!")
        else:
            print(f"You have already watched '{self.title}'.")
    
    def info(self):
        watched_status = "watched" if self.is_watched else "not watched"
        print(f"Title: {self.title}")
        print(f"Director: {self.director}")
        print(f"Year: {self.year}")
        print(f"Genre: {self.genre}")
        print(f"Duration: {self.duration} minutes")
        print(f"Watched: {watched_status}")

# Example usage:
if __name__ == "__main__":
    film1 = Film("Inception", "Christopher Nolan", 2010, "Sci-Fi", 148)
    film2 = Film("The Dark Knight", "Christopher Nolan", 2008, "Action", 152)
    
    film1.watch()
    film1.info()
    
    film2.watch()
    film2.info()
    
    film1.watch()
    film2.watch()

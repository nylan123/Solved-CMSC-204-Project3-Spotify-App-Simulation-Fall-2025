# Solved-CMSC-204-Project3-Spotify-App-Simulation-Fall-2025
 Email Us: jarviscodinghub@gmail.com

https://jarviscodinghub.com/assignment/solved-cmsc-204-project3-spotify-app-simulation-fall-2025/

In this project, you will simulate a simplified version of Spotify that allows users to manage playlists and songs and supports adding and removing elements from both ends of the list. You will implement your own GenericLinkedList class that provides a ListIterator to navigate and remove linked data. The GUI is provided and interacts with your code through clearly defined method interfaces.

Learning Objectives

Implement a generic linked list with a ListIterator.
Use the implemented linked list data structure to represent real-world concepts such as users, playlists, and songs.
Parse text-based user data from a file and create object representations.
Write test cases using JUnit to verify correctness of your linked list and user manager logic.
 

Project Requirements

Implement a GenericLinkedList<T> that implements an Iterable<T> interface supporting forward and backward traversal.
Manage a playlist of songs using the Playlist class and the GenericLinkedList<Song>.
Support navigation (next, previous) through songs in a playlist.
Parse and load users and playlists from a file (format provided).
Properly handle exceptions when invalid input is encountered.
Provided Classes

 

You will receive the following starter code:

GUI
WarehouseSwingApp.java – A small Java Swing GUI that demonstrates the simulation visually.

 

Public JUnit Tests
java– Tests minimum project requirements.
GenericLinkedListPublicTest.java – Tests linked list functionality.
java – Tests Play list functionality.
java – Basic tests for your simulation logic.
 

Required Classes

You must fully implement the following classes:

GenericLinkedList<T> with a ListIterator that provides forward and backward iteration of the list as well as removing the node that is returned by next() or previous() methods of this iterator.
Song, represent a song with the title of the song and the name of the artist.
PlayList, represents a list of songs.
User, represents a user with user name and password and multiple playlists.
Exception classes: UserNotFoundException, InvalidUserFormatException, InvalidPasswordException.
SpotifyManager,represents a list of users and is responsible for loading data from a text file to the list and finding a user by its username and password.
Class methods

 

Your code must include the following methods at minimum. These are required to pass the provided JUnit tests. You may add any additional attributes or methods to your classes.

 

GenericLinkedList<T> Class

Boolean contains(Telement),Checks if the list contains the specified element.
T get(int index),Returns the element at the specified position in this list.
T getFirst(),Gets the first element in the list without removing it.
T getLast(),Gets the last element in the list without removing it.
Boolean isEmpty(),Checks if the list is empty.
ListIterator<T> iterator(),Returns a list iterator over the elements in the list.
T remove(int index),Removes the element at the specified index from the list. IndexOutOfBoundsException– if the index is out of range
Boolean remove(Telement),Removes the first occurrence of the specified element from the list.
T removeFirst(),Removes and returns the first element from the list. throws NoSuchElementException if the list is empty
T removeLast(),Removes and returns the last element from the list. throws NoSuchElementException if the list is empty
int size(), Gets the number of elements in the list.
Object[] toArray(),Converts the linked list to an array containing all of its elements in the same order of the current linkedlist.
GenericIterator (Inner Class in GenericLinkedList )

This Inner class implements the ListIterator Interface and supports only the following methods. For all the other unsupported methods, your code should throw UnsupportedOperationException exception:

hasNext()
next()
hasPrevious()
previous()
remove(),Removes the Node was returned by previous() or next() method. Throws IllegalStateException if next() or previous()has not been called before remove(), or if remove()has already been called after the last next()or previous()
 

Song

This is a simple class that represent a song by title and artist name. You may add constructor(s), getters, setters and any other method that is required.

 

PlayList

This class represents a playlist by its name and a list of songs in the playlist. The following methods are supported by this class:

Boolean addSong(Song song)
Song getCurrentSong()
int getSize()
GenericLinkedList<Song> getSongs() //Returns the shallow
//copy of the list
Boolean isEmpty()
Song nextSong()
Song previousSong()
Boolean removeSong(Song song)
 

 

User

This class represent a user with a name and password and multiple playlists. The following methods are supported by this class:

Void addPlaylist(Playlist playlist)
int getPlaylistCount()
 

SpotifyManager

This class represent a manager class holding multiple users. The following methods are supported by this class:

void loadUsersFromFile(String filename) throws IOException, InvalidUserFormatException
public User findUser(String username, String password) throws UserNotFoundException, InvalidPasswordException
 

Sample users.txt

# USER

username: demo

password: DM

playlist: Pop Playlist

song: Blinding Lights – The Weeknd

song: Levitating – Dua Lipa

song: Imagine – John Lennon

song: Hello – Adele

playlist: Workout

song: Stronger – Kanye West

song: Can’t Hold Us – Macklemore

playlist: Jazz Chill

song: Take Five – Dave Brubeck

 

# USER

username: alice

password: 123

playlist: Chill Vibes

song: Watermelon Sugar – Harry Styles

song: Lost in Japan – Shawn Mendes

Testing Notes

The provided GFA (Good Faith Attempt) JUnit tests represent the minimum requirements to validate the basic functionality of your project. If the project due date has passed, your submission must pass these tests in order to be considered for course credit.
In addition to the GFA tests, any GUI code and public JUnit tests are provided to assist with basic verification of your implementation. However, these do not cover all functionality. You are expected to design and run additional tests to ensure the full correctness and robustness of your project.

 

 

Sample GUI Output

Choosing the file to read user information:

 

 

 

 

 

 

Enter username and password to display the playlist:

 

 

 

 

User’s playlist and songs in the selected playlist:              Playing Next Song:

 

 

 

 

 

 

 

Removing song from playlist:

 

 

 

 

 

 

 

 

Adding a new song:

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

Deliverables

 

Before submitting your project, ensure your code is free of syntax errors. Submissions that do not compile will receive zero points.

 

Design Documents UML and/or Pseudo-Code

 

Implementation Only submit files that you have created or modified, do not submit unmodified files that were provided in the project download. Place all your .java files inside a src folder. Include the entire doc folder with Javadoc for your own classes.

 

Summary Write-Up A 2-3 paragraph write-up (eg.LearningExperience.doc)

 

Submission Packaging

You will submit two compressed .zip files:

Main Project Files All student created or modified project files and data:

Filename LastNameFirstName_AssignmentX.zip

src/ directory containing .java files created or modified by the student

doc/ directory containing student created Javadoc files

LearningExperience.doc reflection and write-up

Design Documents all design related documents

 

MOSS files Only the student created or modified source code files

Filename LastNameFirstName_AssignmentX_Moss.zip

source files only the .java files created or modified by the student

 

Grading Rubric

Criteria	Points
GenericLinkedList Implementation	40%
PlayList Implementation	20%
SpotifyManager Implementation	20%
User and Song Implementation	20%
JUnit student-written tests	-5%
Design and Reflection write-up	-10%
Code style, documentation, and Javadoc (If not provided).	-5%

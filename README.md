# Guess-the-number-game-in-C++
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main()
{
	int num, guess,tries=0;
	srand(time(0)); 
	num = rand() % 100 + 1; 
	cout << "Welcome to Guess the Number Game\n\n";

	do
	{
		cout << "Enter a guess between 1 and 100 : ";
		cin >> guess;
       tries++;
		if (guess > num)
			cout << "Too high!"<<endl;
		else if (guess < num)
			cout << "Too low!"<<endl;
		else
			cout << "\nCorrect! You got it!"<<endl;
	} while (guess != num);
      
      cout<<"Total tries are:"<<tries<<endl;
	return 0;
}

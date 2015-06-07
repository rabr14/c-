# c-
#include <string>
#include <cstdlib>
#include <ctime>
#include <fstream>
using namespace std;

int main(){
	setlocale(0, "swedish");
	unsigned seed;
	string player;
	seed = time(0);
	srand(seed);
	int randomNumber = rand() % 100 + 1;
	bool game = true;
	int number1, number2, number3 = 0;
	int numPlayers = 0;
	int arrayOfData[numberOfElements];
	string arrayOfNames[numberOfNames];
	cout << "vad är spelarens namn?(max 4 spelare): ";
	int winner = 0;
	cin >> player;
	arrayOfNames[numPlayers] = player;
	while (game == true){
		

		cout << "Tal1: ";
		cin >> number1;
		cout << "Tal2: ";
		cin >> number2;
		cout << "Tal3: ";
		cin >> number3;
		numPlayers++;
		
		system("CLS");
		cout << "vad är spelarens namn?: ";
		cin >> player;
		if (player == "Ingen"){
			game = false;
		}
	}

	for (int i = 0; i < numPlayers*3; i++)
	{
		
	
	}

	for (int i = 0; i < numPlayers * 3; i++){
		if (arrayOfData[i] == randomNumber){
			int j = i % 3;
			cout << "Vinnaren är " << arrayOfNames[j] << " som gissade " << arrayOfData[i] << "." << endl;
			winner++;
		}
	}
	if (winner == 0){
		cout << "Ingen kunde gissa talet som var " << randomNumber << endl;
	}
	
	return 0;
}

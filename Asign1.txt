void sortStringArrayAsc(char stringArray[10][MAXLENGTH]){					//to sort string of arrays
	int i,j;
	printf("\nAscending Order\n");
	for(i=0;i<(10-1);i++){									//bubble sort
		for(j=0;j<(10-i-1);j++){
			if(strcmp(stringArray[j],stringArray[j+1]) > 0){
				swapTwoStrings(stringArray[j],stringArray[j+1]);
			}
		}
	}
	printString(stringArray);
	printf("String with lowest ASCII value : %s",stringArray[0]);
	printf("String with highest ASCII value : %s",stringArray[9]);
}
void sortStringArrayDsc(char stringArray[10][MAXLENGTH]){					//to sort string of arrays in desc
	int i,j;
	printf("\nDescending Order\n");
        for(i=0;i<(10-1);i++){									//bubble sort
                for(j=0;j<(10-i-1);j++){		
                        if(strcmp(stringArray[j],stringArray[j+1]) < 0){
                                swapTwoStrings(stringArray[j],stringArray[j+1]);
                        }
                }
        }
        printString(stringArray);
	printf("String with lowest ASCII value : %s",stringArray[9]);
        printf("String with highest ASCII value : %s",stringArray[0]);
}

void swapTwoStrings(char *string1, char *string2){						//swap two strings
	char temp[MAXLENGTH];
	strcpy(temp, string1);
	strcpy(string1, string2);
	strcpy(string2, temp);
}

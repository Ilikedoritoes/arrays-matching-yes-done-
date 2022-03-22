

#include <stdlib.h>
#include <stdio.h>
#define row 3
#define colume 3
#define _CRT_SECURE_NO_WARNINGS

	int main()
	{
		int x, y, amount = 0, amount2 = 0, value;
		printf("please enter %d x %d numbers.\n", row, colume);
		int mtrx[row][colume];
		int mtrx2[row][colume];


		for (x = 0; x < row; x++)
		{
			for (y = 0; y < colume; y++)
			{
				scanf_s("%d", &mtrx[x][y]);
			}
		}

		printf("please enter the second one!\n");

		for (x = 0; x < row; x++)
		{
			for (y = 0; y < colume; y++)
			{
				scanf_s("%d", &mtrx2[x][y]);
			}
		}


		for (x = 0; x < row; x++)
		{
			for (y = 0; y < colume; y++)
			{
				value = mtrx[x][y]; //<----- כול פעם הערך הזה משתנה ולמטה נבדק עם הכמות פעמים שהוא מופיע בכול אחד מהם שווה

				for (x = 0; x < row; x++)
				{
					for (y = 0; y < colume; y++)
					{
						//מעלה את הכמות פעמים שמספר
						// "value"
						// מופיע בהם
					
						if (mtrx[x][y] == value)
							amount++;
						if (mtrx2[x][y] == value)
							amount2++;
					}
				}

				if (amount == amount2)
					flag++;
			}
		}

		if (flag == 1)
			printf("the arrays have the same numbers");
		else
			printf("the arrays dont have the same numbers");

		system("pause");

	}

# Renovation

package Assignment2;

import java.util.Scanner;

public class RenovationProject 
{

	public static void main(String[] args) {
		
		Scanner getData = new Scanner(System.in);
		
		
		// Declaring variable below which are double here
		
		double roomLength, roomWidth, roomHeight, roomWallArea, roomFloorArea;  // Dimensions for the room
		
		double doorWidth, doorHeight, doorArea; // Dimensions for the door
		
		double window1Width, window1Height, window1Area; // Dimensions for the first window
		
		double window2Width, window2Height, window2Area; // Dimensions for the second window
		
		double bookshelfLength, bookshelfHeight, bookshelfDepth, bookshelfFloorArea, bookshelfWallArea; // Dimensions for the bookshelf
		
		double wallPaintArea, floorCarpetArea; // Declares paint area for wall, carpet area for floor
		
		double paintCostPerSqFt, carpetCostPerSqFt, costToPaintWall, costToCarpetFloor; // Declares cost per sq. ft for wall and carpeting floor and their individual costs
		
		// User input request
		System.out.print("Enter the length for room in feet: "); 
		roomLength = getData.nextDouble();
		
		System.out.print("Enter the width for room in feet: ");
		roomWidth = getData.nextDouble();
		
		System.out.print("Enter the height for room in feet: ");
		roomHeight = getData.nextDouble();
		
		System.out.print("Enter the width for door in feet: ");
		doorWidth = getData.nextDouble();
		
		System.out.print("Enter the height for door in feet: ");
		doorHeight = getData.nextDouble();
		
		System.out.print("Enter the width for first window in feet: ");
		window1Width = getData.nextDouble();
		
		System.out.print("Enter the height for first window in feet: ");
		window1Height = getData.nextDouble();
		
		System.out.print("Enter the width for second window in feet: ");
		window2Width = getData.nextDouble();
		
		System.out.print("Enter the height for second window in feet: ");
		window2Height = getData.nextDouble();
		
		System.out.print("Enter the length for bookshelf in feet: ");
		bookshelfLength = getData.nextDouble();
		
		System.out.print("Enter the height for bookshelf in feet: ");
		bookshelfHeight = getData.nextDouble();
		
		System.out.print("Enter the depth for bookshelf in feet: ");
		bookshelfDepth = getData.nextDouble();
		
		System.out.printf("Enter the cost per square foot for painting the wall ($): ");
		paintCostPerSqFt = getData.nextDouble();
		
		System.out.printf("Enter the cost per square foot for carpeting the floor ($): ");
		carpetCostPerSqFt = getData.nextDouble();
		
		// Area calculation
		roomFloorArea = (roomLength * roomWidth);  // Total floor area
		roomWallArea = (roomHeight * roomLength * 2) + (roomWidth * roomHeight * 2); //Total room area
		
		// Area calculation for door, two windows, and bookshelf's floor and wall area
		doorArea = (doorWidth * doorHeight);
		window1Area = (window1Width * window1Height);
		window2Area = (window2Width * window2Height);
		bookshelfFloorArea = (bookshelfLength * bookshelfDepth);
		bookshelfWallArea = (bookshelfLength * bookshelfHeight);
		

		wallPaintArea = (roomWallArea - (doorArea + window1Area + window2Area + bookshelfWallArea)); // Final room area calculation after deducting areas of door, two windows and bookshelf	
		floorCarpetArea = (roomFloorArea - bookshelfFloorArea); //Final floor area calculation after deducting bookshelf area
		costToPaintWall = (wallPaintArea * paintCostPerSqFt); // Calculating cost to paint wall by multiplying paint cost per sq. ft
		costToCarpetFloor = (floorCarpetArea * carpetCostPerSqFt); //Calculating cost to carpet floor by multiplying carpet cost sq.ft
		
		// Output in sq. ft and USD
		System.out.printf("%nThe wall area to be painted is %.2f square feet.%n", wallPaintArea);
		System.out.printf("The floor area to be painted is %.2f square feet.%n", floorCarpetArea);
		System.out.printf("The cost to paint the wall is $%.2f per square feet.%n", costToPaintWall);
		System.out.printf("The cost to carpet the floor is $%.2f per square feet.%n", costToCarpetFloor);
		
		getData.close();
	
	}

}


OUTPUT

Enter the length for room in feet: 12.75
Enter the width for room in feet: 11.25
Enter the height for room in feet: 12
Enter the width for door in feet: 1.95
Enter the height for door in feet: 10
Enter the width for first window in feet: 2.5
Enter the height for first window in feet: 5
Enter the width for second window in feet: 6.8
Enter the height for second window in feet: 7.2
Enter the length for bookshelf in feet: 8
Enter the height for bookshelf in feet: 6
Enter the depth for bookshelf in feet: 3
Enter the cost per square foot for painting the wall ($): 0.95
Enter the cost per square foot for carpeting the floor ($): 1.25

The wall area to be painted is 447.04 square feet.
The floor area to be painted is 119.44 square feet.
The cost to paint the wall is $424.69 per square feet.
The cost to carpet the floor is $149.30 per square feet.



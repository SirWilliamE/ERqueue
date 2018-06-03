/*
 * Code by: William Colachicco
 * Implements a queue for an emergency room
 * In a loop, accepts a new patient name along with priority
 * Each time through the loop, prints out the current list in priority order
 */

import java.util.*;

public class ERqueue {

	public static void main(String[] args) {

		ArrayList<Patient> patients = new ArrayList<>();
		
		while (true) {
			Scanner input = new Scanner(System.in);
			System.out.print("Enter patient name ('exit' to exit): ");
			String name = input.nextLine();
			if (name.toLowerCase().equals("exit"))
				break;
			System.out.print("Enter patient priority: ");
			int priority = input.nextInt();

			Patient patient = new Patient();
			patient.name = name;
			patient.priority = priority;

			patients.add(patient);

			Collections.sort(patients, (p1, p2) -> p2.priority - p1.priority);

			System.out.print("The queue so far: ");
			System.out.println(patients);
		}
	}
}

class Patient {
	public String name;
	public int priority;

	@Override
	public String toString() {
		return "'" + name + ", " + priority + "'";
	}
}

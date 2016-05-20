# time-calc
time calculator program

import javax.swing.JOptionPane;

public class TimeCalc
{
    public static void main(String[] args)
    {
        double seconds;
        String input;

        //constants
        final double SECONDS_PER_MINUTES = 60.0;
        final double SECONDS_PER_HOUR = 3600.0;
        final double SECONDS_PER_DAY = 86400.0;

        //get the number of seconds
        input = JOptionPane.showInputDialog("Eneter the number of seconds.");
        seconds = Double.parseDouble(input);

        //display the number of minutes if any
        if (seconds >= SECONDS_PER_MINUTES)
        {
            //calculate the number of minutes
            double minutes = seconds / SECONDS_PER_MINUTES;

            //display the number of minutes
            JOptionPane.showMessageDialog(null, "There are " +
                        minutes + " minutes in " + seconds + "seconds. ");

        }
        //calculate the number of hours if any
        if (seconds >= SECONDS_PER_HOUR)
        {
            //calculate the number of hours
            double hours = seconds / SECONDS_PER_HOUR;

            //display the number of hours
            JOptionPane.showMessageDialog(null, "There are " +
                        hours + " hours in " + seconds + " seconds. ");

        }
        //calculate the number of days if any
        if (seconds >= SECONDS_PER_DAY)
        {
            //calculate the number of days
            double days = seconds / SECONDS_PER_DAY;

            //display the number of days
            JOptionPane.showMessageDialog(null,"There are " +
                        days + " days in " + seconds + " seconds. ");

        }
        System.exit(0);

    }
}

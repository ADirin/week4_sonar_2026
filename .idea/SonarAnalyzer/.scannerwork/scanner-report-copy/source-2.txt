package org.example;

import java.util.logging.Level;
import java.util.logging.Logger;

public class Calculator {
    public static void main(String[] args) {
        Logger logger = Logger.getLogger(Calculator.class.getName());

        // Only evaluate methods if INFO level is enabled
        if (logger.isLoggable(Level.INFO)) {
            int subResult = subMe(12, 2);
            int addResult = addMe(12, 2);
            int mulResult = mulMe(12, 2);

            logger.info("sub me " + subResult);
            logger.info("add me " + addResult);
            logger.info("mul me " + mulResult);
            logger.info("Addme " + addResult);
        }
    }

    public static int addMe(int a, int b) {
        return a + b;
    }

    public static int subMe(int a, int b) {
        return a - b;
    }

    public static int mulMe(int a, int b) {
        return a * b;
    }
}
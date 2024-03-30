public static List<Integer> gradingStudents(List<Integer> grades) {
      List<Integer> roundedGrades = new ArrayList<>();
        for (int grade : grades) {
            if (grade < 38) {
                roundedGrades.add(grade);
            } else {
                int  Multiple=((grade + 4) / 5) * 5;
                if (Multiple -grade < 3) {
                    roundedGrades.add(Multiple);
                } else {
                    roundedGrades.add(grade);
                }
            }
        }
        return roundedGrades;
    }
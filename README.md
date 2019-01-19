##  Quiz Application ## 
* An interactive quiz application which shows 5 questions on the interface, one by one.
* Questions are retrieved randomly from SQLite database. (The database is scalable. Can
  add any no of questions. Currently the app contains 50 questions)
* Calculates the total score and shows the result at the end.

*Learn from this web: https://www.javatpoint.com/android-sqlite-tutorial

What's new

1. Add score
2. Add highscore
3. Number of question will display result
4. Using shared preference to keep value

//tosavehighscore
 public void setHighscore(int score){
        final SharedPreferences sharedPreferences = getSharedPreferences("Result", Context.MODE_PRIVATE);
        int highScore=sharedPreferences.getInt(result,0);
        if(score > highScore){
            SharedPreferences.Editor editor=sharedPreferences.edit();
            editor.putInt(result,score);
            editor.commit();
        }
    }
//get
    public int getHighScore(){
        final SharedPreferences sharedPreferences = getSharedPreferences("Result", Context.MODE_PRIVATE);
        return sharedPreferences.getInt(result,score);
    }

#### Screenshots ####

![Alt text](quizapp.png?raw=true "Title")

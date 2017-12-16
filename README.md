# court-counter-
android development intermediate
java code for cc
package com.example.android.courtcounter;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    int scoreA=0;
    int scoreB=0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    /**
     * Displays the given score for Team A.
     */
    public void displayForTeamA(int score) {
        TextView scoreView = (TextView) findViewById(R.id.team_a_score);
        scoreView.setText(String.valueOf(score));
    }
    public void increment3(View View) {
        scoreA=scoreA+3;
        displayForTeamA(scoreA);
    }
    public void increment2(View view) {
        scoreA=scoreA+2;
        displayForTeamA(scoreA);
    }
    public void increment1(View view) {
        scoreA=scoreA+1;
        displayForTeamA(scoreA);
    }
    public void displayForTeamB(int score) {
        TextView scoreView = (TextView) findViewById(R.id.team_b_score);
        scoreView.setText(String.valueOf(score));
    }
    public void increment3B(View View) {
        scoreB=scoreB+3;
        displayForTeamB(scoreB);
    }
    public void increment2B(View view) {
        scoreB=scoreB+2;
        displayForTeamB(scoreB);
    }
    public void increment1B(View view) {
        scoreB=scoreB+1;
        displayForTeamB(scoreB);
    }
    public void resetscore(View View) {
        scoreA=0;
        scoreB=0;
        displayForTeamA(scoreA);
        displayForTeamB(scoreB);
    }

}

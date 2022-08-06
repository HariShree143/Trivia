# Trivia
Trivia is app that answers the questions of a request
create-react-app-trivia;
 trivia && npm ; start;
 import {useState, useEffect} from 'react';
//opentdb.com/api.php?amount=1

 const [questions, setQuestions] = useState([])
const [loaded, setLoaded] = useState(false)
const [qInd, setQInd] = useState(0)
async function loadQuestions() {
    let response = fetch(url).then(response => response.json()).then(data => {
        setQuestions(data.results);
        setLoaded(true);
    });
}
    retu(
        <div className="App">
          {loaded && <div>
          <p className = "Question">{questions[qInd].question}</p>
          </div>
          }
        </div>
       );
       const loadQuestions = async () => {
        let response = fetch(url).then(response => response.json()).then(data =>       {
           insertCorr(data.results[0].incorrect_answers, data.results[0].correct_answer)
           setQuestions(data.results)
           setLoaded(true)
          })
        }
        function insertCorr(arr, corr) {
            const randInd = Math.floor(Math.random() * 4)
            arr.splice(randInd, 0, corr)
        }
        retu(
            <div className="App">
              {loaded && <div>
              <p className = "Question">{questions[qInd].question}</p>
               {questions[qInd].incorrect_answers.map((a) => {
                return <button key = {a} onClick = {(e) => handlePrsd(e, a)}>{a}</button>
               })}
              </div>
              }
            </div>
           );
           function handlePrsd(e, ans) {
    e.preventDefault();
    if (qInd + 1 < questions.length) {
        insertCorr(questions[qInd + 1].incorrect_answers, questions[qInd + 1].correct_answer);
        setQInd(qInd + 1);
    } else {
        loadQuestions();
        setQInd(0);
    }
}
         const [score, setScore] = useState(0)
const [lastAns , setLastAns] = useState('black')
<p ; const className = "Score" ;style; {{color: lastAns}}Score; {score} p>
    function handlePrsd(e, ans) {
        e.preventDefault();

        if (ans == questions[qInd].correct_answer) {
            setScore(score + 10);
            setLastAns('green');
        } else {
            setScore(score - 10);
            setLastAns('red');
        }
        if (qInd + 1 < questions.length) {
            insertCorr(questions[qInd + 1].incorrect_answers, questions[qInd + 1].correct_answer);
            setQInd(qInd + 1);
        } else {
            loadQuestions();
            setQInd(0);
        }
    }
 {
    display: flex;
    flex-direction; column;
    align-items; center;
    width: 100%
    height; 100%
    padding-top; 100 ;px;
    text-align; center;
  }
  button; {
    color: black;
    text-decoration; none;
    background: 1;b;95;db;
    padding: 20;px;
    border-radius; 10;px;
    font-size; 22;px;
    display: inline-block;
    border: none;
    transition: all; 0.4; ease; 0
    margin: 20;px;
    border: 2;px; solid; black;
  }
  button:hover; {
    background: 3;db;1;f5;
  }
  Question; {
    font-size; 32;px;
    margin-right; 50;px;
    margin-left; 50;px;
  }
  Score; {
    font-size; 20;px;
  }
   start;
         

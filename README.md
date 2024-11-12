# tous-et-tout
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercices - Tous vs Tout</title>
    <style>
        .correct { color: green; }
        .incorrect { color: red; }
        .feedback { margin-top: 5px; }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["tous", "tout", "tous", "tout", "tout", "tous", "tout", "tous", "tout", "tous", "tous", "tout", "tout", "tous", "tout", "tous", "tout", "tous", "tout", "tous"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✅ Correct";
                    feedback.className = "correct feedback";
                    score++;
                } else {
                    feedback.innerText = `❌ Incorrect. La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "tous" s'emploie quand on parle de plusieurs éléments (ex: "tous les enfants"), tandis que "tout" est utilisé pour désigner une totalité ou quelque chose d'indéfini (ex: "tout est prêt").`;
                    feedback.className = "incorrect feedback";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>
<body>
    <h2>Exercices - Complétez avec "tous" ou "tout"</h2>

    <p><strong>Règle :</strong> "Tous" s'utilise quand on parle de plusieurs éléments (ex : "tous les enfants"). "Tout" est utilisé pour désigner une totalité ou une notion indéfinie (ex : "tout est prêt").</p>

    <form>
        <ol>
            <li>___ les élèves sont présents. <input type="text" id="reponse1"> <span id="feedback1"></span></li>
            <li>___ est prêt pour le voyage. <input type="text" id="reponse2"> <span id="feedback2"></span></li>
            <li>J'ai invité ___ mes amis. <input type="text" id="reponse3"> <span id="feedback3"></span></li>
            <li>Il a mangé ___ le gâteau. <input type="text" id="reponse4"> <span id="feedback4"></span></li>
            <li>___ ce que tu dis est intéressant. <input type="text" id="reponse5"> <span id="feedback5"></span></li>
            <li>___ les chats du quartier sont ici. <input type="text" id="reponse6"> <span id="feedback6"></span></li>
            <li>___ est bien organisé. <input type="text" id="reponse7"> <span id="feedback7"></span></li>
            <li>Ils ont fini ___ leurs devoirs. <input type="text" id="reponse8"> <span id="feedback8"></span></li>
            <li>___ est en ordre. <input type="text" id="reponse9"> <span id="feedback9"></span></li>
            <li>___ les enfants jouent dehors. <input type="text" id="reponse10"> <span id="feedback10"></span></li>
            <li>___ les livres ont été rangés. <input type="text" id="reponse11"> <span id="feedback11"></span></li>
            <li>___ s'est bien passé. <input type="text" id="reponse12"> <span id="feedback12"></span></li>
            <li>___ le monde est ici. <input type="text" id="reponse13"> <span id="feedback13"></span></li>
            <li>Ils ont appelé ___ leurs amis. <input type="text" id="reponse14"> <span id="feedback14"></span></li>
            <li>___ est parti sans prévenir. <input type="text" id="reponse15"> <span id="feedback15"></span></li>
            <li>Ils ont trouvé ___ ce qu'ils cherchaient. <input type="text" id="reponse16"> <span id="feedback16"></span></li>
            <li>Elle a pris ___ son courage à deux mains. <input type="text" id="reponse17"> <span id="feedback17"></span></li>
            <li>___ les détails ont été vérifiés. <input type="text" id="reponse18"> <span id="feedback18"></span></li>
            <li>___ est prêt pour la fête. <input type="text" id="reponse19"> <span id="feedback19"></span></li>
            <li>Ils ont perdu ___ leurs clés. <input type="text" id="reponse20"> <span id="feedback20"></span></li>
        </ol>

        <button type="button" onclick="verifier()">Vérifier</button>
    </form>

    <p id="score"></p>
</body>
</html>

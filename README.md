foreach ($MP as $row) { 

echo "<div class='mySlides'><div class='heros-text-postac'>Nazwa konta: ".$row['nazwa']."<br>Profesja: ".$class[$row['klasa']]."<br>Poziom: ".$row['poziom']."</div>"
        . "<br><br> "
        . "<a class='play' href='?page=zalogowany&loggedAcc=".htmlentities($row['id_konta'])."'>"
        . "<img class='heros-play' src='public/images/play.png'></a> "
        . "<br><br><a class='minus' href='?page=zalogowany&deleteAcc=".htmlentities($row['id_konta'])."'><img src='public/images/x.png'> <span class='minus_a'>usuń postać ".htmlentities($row['nazwa'])." </span></a><br><br>"
        . "<div>
    <a class='minus'>
        <span onclick='document.getElementById(\"id01\").style.display=\"block\" class='minus_a'>
            <img src='public/images/x.png'> 
            Usuń postać nick
        </span>
    </a>

  <div id='id01' class='w3-modal w3-animate-opacity'>
      <div class='w3-modal-content'><br>
        <div class='heros-header-del'>Czy jesteś pewien, że chcesz usunąć swoją postać?</div>
      
        <div class='heros-text-del'><br>
        Twoja postać zostanie usunięta. <br>I nie będzie można jej odzyskać w żaden sposób.
        </div>
     
        <div class='heros-button-del'>
            
            <a href='?page=zalogowany&deleteAcc= ".htmlentities($row['id_konta'])."'> <img class='heros-button-del-acc' src='public/images/accept.png'></a> </a>
            
                <span onclick='document.getElementById(\"id01\").style.display=\"none\"'><img class='heros-button-del-cancel' src='public/images/cancel.png'></a></span>
            
        </div>
      
    </div>
  </div>
</div>
</div>";
     
}

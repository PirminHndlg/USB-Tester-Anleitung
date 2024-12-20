<h1>Anleitung zum USB Tester Löt Kit</h1>

<div class="img-container">
    <img src="Website/3.jpeg">
</div>

<h4>Enthaltene Komponenten</h4>
<ul>
    <li>1x pcb</li>
    <li>2x USB Typ-C Buchse (teilweise schon an pcb angelötet)</li>
    <li>1x USB Typ-A 3.0 Buchse</li>
    <li>1x Micro USB Typ-B Buchse</li>
    <li>1x Mini USB Typ-B Buchse</li>
    <li>1x USB Typ-B 3.0 Buchse</li>
    <li>1x Batterie Halterung</li>
    <li>30x Widerstand 2.2kΩ (25 + 5 Reserve)</li>
    <li>30x LEDs gelb (25 + 5 Reserve)</li>
    <li>1x Kondensator 10μF</li>
</ul>

<div class="img-container">
    <img src="Website/1.jpg" alt="Komponentenübersicht">
</div>

<p style="background-color: green; padding: 10px"><strong>Hinweis:</strong> Bei der USB-C Buchse auf der rechten Seite
    kann es sein, dass sich einige Pins untereinander brücken. Das ist kein Problem! Die Kontakte auf dem pcb sind
    sowieso mit einer VCC-Plane verbunden. Auf der linken Seite darf es aber nicht sein!</p>

<h4>Anleitung</h4>
<ol>
    <li>
        Löte die Widerstände und die LEDs auf die Platine, die oberen Kontakte sind für die Widerstände und die
        unteren für die LEDs
        <p style="background-color: red; padding: 10px"><strong>Wichtig:</strong> die LEDs haben eine Ausrichtung!</p>
        <div class="Website/img-container">
            <img src="Website/7.jpeg" alt="Close-Up auf LED-Rückseite">
        </div>
        Auf der Rückseite der LED sieht man eine Markierung für die Kontakte. Der Kontakt mit dem Kreuz ist der Minuspol
        und muss an den linken Kontakt der Platine mit der vollständigen Umrandung gelötet werden.
        <div class="Website/img-container">
            <img src="Website/8.jpeg" alt="Close-Up auf LED und Widerstand">
        </div>
        Auf der Vorderseite ist die Unterscheidung der beiden Kontakte der LEDs leider nur schwer zu erkennen, aber der
        Pluspol hat zwei kleine Streifen und der Minuspol nur einen.
        <br><br>
        12 LEDs + Widerstände sind für die linke Seite der Platine und 12 für die rechte Seite bestimmt. Das letze Paar
        kommt unten in die linke Ecke der Platine bei der Aufschrift "SHIELD".
    </li>
    <li>
        Löte die Buchsen auf die Platine. Anordnung siehe Bild. Für die Stecker auf der rechten Seite spielt es
        keine Rolle, ob einzelne Kontakte sich untereinander berühren und einen Kurzschluss bilden.
        <div class="img-container">
            <img src="Website/2.jpeg" alt="Bild von Vorderseite">
            <img src="Website/4.jpeg" alt="Bild von Rückseite">
        </div>
        Falls die USB-C Buchsen noch nicht angelötet sind, ist das der schwierigste Teil. Ich war am erfolgreichsten,
        indem ich die mit Reflow-Löten angelötet habe.
        <p style="background-color: orange; padding: 10px"><strong>Hinweis:</strong> Bei der Micro-USB-B-Buche habe ich einen kleinen Fehler beim pcb gemacht. Diese muss sich das eine Bein mit einer USB-C-Buchse teilen. Gequetscht sollte aber alles nebeneinander passen.</p>
    </li>
    <li>
        Löte den Kondensator an die richtige Stelle neben dem Pluspol der Batterie. Die Ausrichtung spielt keine Rolle.
        <div class="img-container">
            <img src="Website/6.jpg" alt="Close-Up auf Kondensator">
        </div>
    </li>
    <li>
        Löte die Batterie-Halterung an. Achte auf die richtige Polung! Es gibt eine kleine Markierung an der Ecke der
        Halterung für den Plus- und Minuspol.
    </li>
    <li>
        Und fertig ist dein USB Tester! Viel Spass beim Testen von USB-Kabeln!
    </li>
</ol>

<h3 style="background-color: red; text-align: center; padding: 10px; border-radius: 10px">Wie es auch überall steht, ist es wichtig, dass man
    den Tester <strong>nicht</strong> an ein Gerät anschließt,
    sondern nur Kabel!</h3>

<div class="img-container">
    <img src="Website/5.jpeg" alt="Bild von fertigem Tester">
</div>

<h4>Weitere Links</h4>

<p><a href="https://github.com/PirminHndlg/USB-Tester-Anleitung/tree/main/Case">Hier</a> gibt eine 3D-Druck-Vorlage für
    ein kleines, einfaches Case.</p>

<p><a href="https://github.com/PirminHndlg/USB-Tester-Anleitung/tree/main/pcb">Hier</a> kann man das KiCad-Projekt zum
    pcb finden. Ich habe das <a href="https://github.com/alvarop/usb_c_cable_tester">Original von alvarop</a> etwas
    angepasst, da einzelne Teile nicht mehr verfügbar waren. Eine aktuelle Liste gibt es <a
            href="https://github.com/PirminHndlg/USB-Tester-Anleitung/blob/main/pcb/LCSC%20Exported%20May%2030%202024.csv">hier</a>
</p>

<h4>Erklärung zur Pin-Belegung</h4>

<div class="table-container">
    <table>
        <tr>
            <th>Charge only</th>
            <td>GND</td>
            <td>VBUS</td>
        </tr>
        <tr>
            <th>USB 2.0</th>
            <td>GND</td>
            <td>VBUS</td>
            <td>D-</td>
            <td>D+</td>
        </tr>
        <tr>
            <th>USB 3.0</th>
            <td>GND</td>
            <td>VBUS</td>
            <td>D-</td>
            <td>D+</td>
            <td>RX-</td>
            <td>RX+</td>
            <td>TX-</td>
            <td>TX+</td>
        </tr>
    </table>
</div>
<p>Bei USB-C als Host (Buchse auf linker Seite) und Client (Buchse auf rechter Seite) leuchten beide Seiten, da dann
    sowohl die A als auch die B Pins verbunden sind. Außerdem sollte mind. ein CC-Pin verbunden sein</p>

<div class="img-container">
    <img style="background-color: white" src="Website/USB Type-C Pinout.png" alt="Pinbelegung von USB C">
</div>

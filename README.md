# PHPFormsII
## get
```HTML
<!-- Als je GEEN action meegeeft aan een form, wordt standaard de huidige pagina gebruikt. (Soms noemt men dit een POSTBACK.) -->

<form method="get">
    <select name="vorm">
        <option value="ovaal">ovale vorm</option>
        <option value="rond">ronde vorm</option>
        <option value="vierkant">vierkante vorm</option>
    </select>
    <select name="kleur">
        <option value="rood">rode kleur</option>
        <option value="blauw">blauw kleur</option>
        <option value="oranje">oranje kleur</option>
    </select>
    <input type="submit" value="Ik heb gekozen!">
</form>

<form> //method="GET" of "POST"
	<input type="text"/>
	<input type="password"/> //elk input element een naam geven: username en password (keys en values) zichtbaar in URL
	//bij https: niet zomaar zichtbaar met sniffer
</form>
<form>
	<input type="radio" name="dier" value="Kat">Kat</input>
	<input type="radio" name="dier" value="Hond">Hond</input>
</form>

<ul>
```
```PHP
<?php
// Vul de juiste key in voor $_GET[...] zodat de gekozen VORM en KLEUR getoond wordt. (anders werkt ie niet)
echo "<li>" . $_GET["vorm"] . "</li>";
echo "<li>" . $_GET["kleur"] . "</li>";
echo "Hallo " . htmlspecialchars($_POST["dier"]) . "!";
?>

</ul>

<h2>Na SUBMIT: Check de URL!</h2>
<p>Waar komen de <em>key</em>- en <em>value</em>-pairs vandaan?</p>
```
geen ``action``: pagina refreshen
POST: ww in body (niet header)
zie ook ... van lk.

## Post.php
```HTML
<form>
	Naam: <input type="text" name="naam"><br>
	E-mailadres: <input type="text" name="email"><br>
	<input type="submit">
</form>
```
```PHP
<?php
echo "Welkom " . $_POST["naam"];
echo "Uw e-mailadres is: " . $_POST["email"];
```

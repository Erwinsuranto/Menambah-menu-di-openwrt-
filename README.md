# Menambah-menu-di-openwrt
STEP PERTAMA
1. Open File Manager usr/share/ucode/luci/template/themes/material/ Open File header.ut
 Atau klik link ini untuk menuju File http://192.168.1.1/tinyfm/tinyfm.php?p=usr%2Fshare%2Fucode%2Fluci%2Ftemplate%2Fthemes%2Fmaterial&view=header.ut
2. Sebelum di edit sebaiknya di backup dulu File original nya
3. Copy File di bawa ini, paste di bawah bawa code </script>
```
<nav id='menu'>
  <input type='checkbox' id='responsive-menu' onclick='updatemenu()'><label></label>
  <ul>
    <li><a href='http://192.168.8.1/' target='_blank'>Modem</a></li>    
    <li><a href='/cgi-bin/luci/admin/services/ttyd'>Terminal</a></li>
	<li><a id="yacd" target='_blank'><p>Yacd</p></a></li>
	<li><a href='https://www.youtube.com/c/IndonesianTechChannel/videos' target='_blank'>Youtube</a></li>
	<li><a href='/cgi-bin/luci/admin/status/about'>About</a></li>
	<script type="text/javascript">document.getElementById("yacd").setAttribute("href", "http://" + window.location.hostname + ":9090/ui/yacd/",);</script>
    <!-- Dropdown untuk AP -->
    <li><a href='#' class="dropdown-arrow">AP</a>
      <ul class="sub-menus">
        <li><a href='http://192.168.1.2' target='_blank'>AP 1</a></li>
        <li><a href='http://192.168.1.3' target='_blank'>AP 2</a></li>
      </ul>
    </li>

    <!-- Dropdown untuk WAN -->
    <li><a href='#' class="dropdown-arrow">Link</a>
      <ul class="sub-menus">
        <li><a href='https://www.speedtest.net/id' target='_blank'>Speedtest</a></li>
        <li><a href='https://my.kmsp-store.com/login' target='_blank'>Kmsp Store</a></li>
        <li><a href='https://d3ward.github.io/toolz/adblock' target='_blank'>D3ward</a></li>
        <li><a href='https://browserleaks.com/dns' target='_blank'>DNS Leak</a></li>
      </ul>
    </li>
  </ul>
</nav>
```
Hasilnya Seperti Gambar Di Bawah Ini
<h1 align="center">
  <img src="https://raw.githubusercontent.com/Erwinsuranto/Menambah-menu-di-openwrt-/main/IMG-20240914-WA0015.jpg" alt="neko" width="500">
</h1>

STEP KEDUA
1. Copy File di bawah ini, paste di bawa code <style>
```
#menu ul.sub-menus {
    height: auto;
    overflow: hidden;
    width: 150px;
    background: #f2f2f2;
    position: absolute;
    z-index: 99;
    display: none;
    padding: 0;
    list-style: none;
}

#menu ul.sub-menus li {
    display: block;
    width: 100%;
}

#menu ul.sub-menus a {
    display: block;
    padding: 10px;
    color: #002b49;
    background: #f2f2f2;
    text-decoration: none;
    font-size: 12px;
}

#menu ul.sub-menus a:hover {
    background: #31b1e7;
    color: #fff;
}

#menu li:hover ul.sub-menus {
    display: block;
}
```
Hasilnya Seperti Gambar Di Bawah Ini

<h1 align="center">
  <img src="https://raw.githubusercontent.com/Erwinsuranto/Menambah-menu-di-openwrt-/main/IMG-20240915-WA0000.jpg" alt="neko" width="500">
</h1>

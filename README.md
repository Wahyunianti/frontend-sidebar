# Tampilan Halaman HTML CSS Javascript Sidebar Dropdown

## Preview

<img width="1680" alt="Screen Shot 2024-10-06 at 14 31 14" src="https://github.com/user-attachments/assets/e6780aa7-379b-417d-9d97-8817661629ec">

## Tech
- HTML 5
- CSS
- Javascript


## Codes

### ul > li
HTML Codes ul li :

```bash

 <ul>
                <li>
                    <input type="checkbox" id="submenu0">
                    <label for="submenu0" class="collapsible">
                        <p>Stock Management</p>
                    </label>
                    <div class="sub-menu">
                        <ul>
                            <li>
                                <a href="">
                                  
                                    <p>Receive Stock</p>
                                </a>
                            </li>
                        </ul>
                    </div>
                </li>
</ul>

```

### CSS Style
CSS codes for sidebar dropdown:

```bash
.sub-menu {
    display: block;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease-out;
}
input[type="checkbox"] {
    display: none;
}
input[type="checkbox"]:checked + .collapsible + .sub-menu {
    max-height: 200px;
}
```

### CSS Style Highlight
CSS codes for disable hightlight:

```bash
li {
    margin-block: 10px;
    padding: 5px;
    cursor: pointer;
    position: relative;
    width: 100%;
    overflow: hidden;
    transition: background-color 0.2s ease;
    -webkit-tap-highlight-color: transparent;
}
```

### Javascript Hamburger
Javascript codes for translate sidebar:

CSS content
```bash
.content {
    display: block;
    margin-left: 16%;
    transition: margin-left 0.3s ease; //important
}
.shifted {
    margin-left: 0; //after
}
```

CSS sidebar
```bash
.sidebar {
    position: fixed;
    transition: transform 0.3s ease;
    transform: translateX(0%);
}
.hidden {
    transform: translateX(-73%);
}
```

Javascript
```bash
document.getElementById('hamburger').addEventListener('click', function() {
    const sidebar = document.getElementById('sidebar');
    const content = document.getElementById('content');
    sidebar.classList.toggle('hidden');
    content.classList.toggle('shifted');
});
```

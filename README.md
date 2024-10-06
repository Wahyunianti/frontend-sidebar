# Tampilan Halaman HTML CSS Javascript Sidebar Dropdown

## Preview


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

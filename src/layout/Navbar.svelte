  <script>
    import { Link } from 'svelte-routing'
    </script>
  
  <nav>
    <div class="nav-wrapper">
    <div class="container">
     <Link to="/" > <span class="brand-logo">svelte tutorial </span></Link>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
      <li><Link to="/"> home </Link></li>
      <li><Link to="/about"> about </Link></li>
           
      </ul>
    </div>
     
    </div>
  </nav>
        
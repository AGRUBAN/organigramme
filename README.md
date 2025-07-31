
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Organigramme Groupe MGD</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f8f9fa;
      margin: 0;
      padding: 20px;
      color: #333;
    }
    .container {
      max-width: 1200px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }
    .logo {
      text-align: center;
      margin-bottom: 20px;
    }
    .logo img {
      max-width: 250px;
    }
    h1 {
      text-align: center;
      color: #2c3e50;
      margin-bottom: 30px;
    }
    .tree, .children {
      display: flex;
      flex-direction: column;
      align-items: center;
      position: relative;
    }
    .node {
      margin: 10px;
      position: relative;
      text-align: center;
    }
    .node-content {
      background: #3498db;
      color: white;
      padding: 15px 20px;
      border-radius: 8px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.1);
      cursor: pointer;
      transition: all 0.3s;
    }
    .node-content:hover {
      transform: translateY(-3px);
    }
    .children {
      flex-direction: row;
      justify-content: center;
      margin-top: 20px;
    }
    .connector {
      width: 2px;
      height: 20px;
      background: #ccc;
      position: absolute;
      top: -20px;
      left: 50%;
      transform: translateX(-50%);
    }
    .hidden {
      display: none;
    }
    .toggle-icon {
      display: inline-block;
      margin-left: 5px;
      font-size: 0.8em;
      transform: rotate(0);
      transition: transform 0.3s;
    }
    .node-content.active .toggle-icon {
      transform: rotate(180deg);
    }
    .note {
      margin-top: 40px;
      text-align: center;
      font-size: 0.85em;
      color: #7f8c8d;
    }
    @media (max-width: 768px) {
      .children {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="logo">
      <img src="https://cdn.prod.website-files.com/65afc0990e6e1ae61d846f55/65afce130399b3705910d6ea_mgd-logo.webp" alt="Logo Groupe MGD" />
    </div>
    <h1>ORGANIGRAMME MGD GROUPE</h1>
    <div class="tree">
      <div class="node">
        <div class="node-content" onclick="toggleChildren(this)">
          <div><strong>ARNAUD MORINET</strong></div>
          <div>Directeur Général</div>
          <span class="toggle-icon">▼</span>
        </div>
        <div class="children hidden">
          <div class="node">
            <div class="connector"></div>
            <div class="node-content" onclick="toggleChildren(this)">
              <div><strong>SYLVIE MORINET</strong></div>
              <div>Directrice RH</div>
              <span class="toggle-icon">▼</span>
            </div>
            <div class="children hidden">
              <div class="node">
                <div class="connector"></div>
                <div class="node-content">
                  <div><strong>ISABELLE GIRAUDET</strong></div>
                  <div>Assistante comptable & RH</div>
                </div>
              </div>
            </div>
          </div>
          <div class="node">
            <div class="connector"></div>
            <div class="node-content" onclick="toggleChildren(this)">
              <div><strong>FREDERIC DERAIN</strong></div>
              <div>Directeur Administratif et Finances</div>
              <span class="toggle-icon">▼</span>
            </div>
            <div class="children hidden">
              <div class="node">
                <div class="connector"></div>
                <div class="node-content">
                  <div><strong>MONICA DOS SANTOS</strong></div>
                  <div>Responsable administrative</div>
                </div>
              </div>
              <div class="node">
                <div class="connector"></div>
                <div class="node-content" onclick="toggleChildren(this)">
                  <div><strong>YOUNES MABROUK</strong></div>
                  <div>Responsable Comptable</div>
                  <span class="toggle-icon">▼</span>
                </div>
                <div class="children hidden">
                  <div class="node">
                    <div class="connector"></div>
                    <div class="node-content">
                      <div><strong>AFIF CHAHID</strong></div>
                      <div>Assistante Comptable</div>
                    </div>
                  </div>
                  <div class="node">
                    <div class="connector"></div>
                    <div class="node-content">
                      <div><strong>NATHALIE</strong></div>
                      <div>Assistante Comptable</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="node">
            <div class="connector"></div>
            <div class="node-content">
              <div><strong>STEPHANE BEGARD</strong></div>
              <div>Directeur d'exploitation</div>
            </div>
          </div>
          <div class="node">
            <div class="connector"></div>
            <div class="node-content">
              <div><strong>INGRID BELGADO</strong></div>
              <div>Directrice d'exploitation</div>
            </div>
          </div>
          <div class="node">
            <div class="connector"></div>
            <div class="node-content">
              <div><strong>LUDOVIC LAROUSSE</strong></div>
              <div>Directeur d'exploitation</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="note">
      Groupe MGD 2025 - Tous droits réservés
    </div>
  </div>
  <script>
    function toggleChildren(el) {
      const parent = el.closest('.node');
      const children = parent.querySelector('.children');
      if (!children) return;
      children.classList.toggle('hidden');
      el.classList.toggle('active');
    }
  </script>
</body>
</html>

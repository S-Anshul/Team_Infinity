<h1> United Airlines Flight Difficulty Analysis</h1>
<p><strong>Team Infinity</strong></p>

<hr>

<h2> Introduction</h2>
<p><strong>Customer:</strong> “My flight to Brussels got delayed again! Is this route always this chaotic?”<br>
<strong>Aditya (Future UA Employee):</strong> “It’s not just bad luck — some flights are naturally harder to manage. Too many transfers, tight schedules, or special requests can make them tricky.”<br>
<strong>Customer:</strong> “So… you can actually measure how difficult a flight is?”<br>
<strong>Anshul (Future UA Employee):</strong> “That’s what we’re trying to figure out.”</p>
<p>This project was born from that very question — can we <strong>quantify flight difficulty</strong>?</p>

<hr>

<h2> Project Overview</h2>
<p>United Airlines operates thousands of flights every day, each with varying levels of operational complexity.</p>
<p>This project introduces the <strong>Flight Difficulty Score (FDS)</strong> — a composite metric that measures how challenging a flight is to operate, based on multiple real-world parameters:</p>
<ul>
    <li> Delays and ground time</li>
    <li> Passenger and baggage load</li>
    <li> Special Service Requests (SSRs)</li>
    <li> Transfer-to-checked bag ratios</li>
</ul>
<p>By analyzing these factors, we classify each flight as <strong>Easy, Medium, or Difficult</strong>, helping airlines optimize operations, resource allocation, and scheduling.</p>

<hr>

<h2> Dataset Description</h2>
<p>All datasets are stored in the <code>Data/</code> folder.</p>
<table>
    <tr>
        <th>Dataset</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>Airports Data</td>
        <td>Airport and country codes</td>
    </tr>
    <tr>
        <td>Bags Data</td>
        <td>Transfer and checked baggage details</td>
    </tr>
    <tr>
        <td>Flights Data</td>
        <td>Flight schedules, delays, fleet, and carrier</td>
    </tr>
    <tr>
        <td>PNR Flight Data</td>
        <td>Passenger details (children, lap infants, etc.)</td>
    </tr>
    <tr>
        <td>PNR Remark Data</td>
        <td>Special Service Requests (SSRs) linked to each passenger</td>
    </tr>
</table>

<hr>

<h2> Analysis Pipeline</h2>

<h3>1️ Data Loading & Cleaning</h3>
<ul>
    <li>Imported and merged all datasets</li>
    <li>Converted date/time columns</li>
    <li>Handled missing and inconsistent data</li>
</ul>

<h3>2️ Feature Engineering</h3>
<ul>
    <li>Calculated new features: delay duration, passenger ratios, ground time flags, SSR counts</li>
    <li>Computed a custom <strong>Flight Difficulty Score (FDS)</strong></li>
</ul>

<h3>3️ Difficulty Classification</h3>
<ul>
    <li>Ranked flights by daily FDS</li>
    <li>Top 20% → Difficult</li>
    <li>Middle 60% → Medium</li>
    <li>Bottom 20% → Easy</li>
</ul>

<h3>4️ Exploratory Data Analysis (EDA)</h3>
<ul>
    <li>Distribution of FDS</li>
    <li>Top 10 most difficult flights</li>
    <li>Difficult destinations</li>
</ul>

<h3>5️ Correlation Analysis</h3>
<ul>
    <li>Found relationships between FDS and features like passenger count, delay, SSRs, and baggage ratios</li>
</ul>

<h3>6️ Visualizations</h3>
<ul>
    <li>Histograms showing FDS distribution</li>
    <li>Bar charts for Top 10 Difficult Flights and Destinations</li>
    <li>Correlation heatmaps for operational insights</li>
</ul>

<hr>

<h2> Key Insights</h2>
<ul>
    <li>Most flights have low difficulty scores, with few highly difficult outliers</li>
    <li>Certain destinations consistently have higher average difficulty</li>
    <li>Strong correlations observed between:
        <ul>
            <li>Passenger count and difficulty</li>
            <li>Tight ground time and delay rate</li>
            <li>SSR count and overall complexity</li>
        </ul>
    </li>
</ul>

<hr>

<h2> Tech Stack</h2>
<ul>
    <li>Python</li>
    <li>pandas, numpy, matplotlib, seaborn</li>
    <li>Jupyter Notebook</li>
</ul>

<hr>

<h2> Usage</h2>
<p>Clone this repository:</p>
<pre>
git clone https://github.com/&lt;your-username&gt;/United_airline_TEAM_INFINITY.git
</pre>

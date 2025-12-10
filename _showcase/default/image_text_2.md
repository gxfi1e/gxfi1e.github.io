---
show: true
width: 4
date: 2020-01-12 00:01:00 +0800
---
<div id="citation-chart" style="height:300px;"></div>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
async function loadCitations() {
    const url = "https://api.semanticscholar.org/graph/v1/author/98318272?fields=papers.year,papers.citationCount";
    const res = await fetch(url);
    const data = await res.json();

    let yearly = {};
    
    data.papers.forEach(p => {
        if (!p.year) return;
        yearly[p.year] = (yearly[p.year] || 0) + p.citationCount;
    });
    
    const years = Object.keys(yearly).sort();
    const citations = years.map(y => yearly[y]);
    
    new Chart(document.getElementById("citation-chart"), {
        type: 'bar',
        data: {
            labels: years,
            datasets: [{
                label: 'Citations per Year',
                data: citations
            }]
        }
    });
}

loadCitations();
</script>


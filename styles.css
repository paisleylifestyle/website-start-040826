async function loadSharedHeader() {
  const target = document.getElementById('site-header-mount');
  if (!target) return;

  try {
    const response = await fetch('header.html');
    const html = await response.text();
    target.innerHTML = html;

    const currentPage = document.body.dataset.page;
    document.querySelectorAll('.nav-link[data-page]').forEach((link) => {
      if (link.dataset.page === currentPage) {
        link.classList.add('active');
      }
    });
  } catch (error) {
    console.error('Header failed to load.', error);
  }
}

document.addEventListener('DOMContentLoaded', loadSharedHeader);

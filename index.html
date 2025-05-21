<html lang="en">
 <head>
  <meta charset="utf-8"/>
  <meta content="width=device-width, initial-scale=1" name="viewport"/>
  <title>
   Alone Flyer's Learning - Notifications
  </title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&amp;display=swap" rel="stylesheet"/>
  <style>
   body {
      font-family: 'Montserrat', sans-serif;
    }
    /* Animation for notification cards */
    @keyframes slideInFade {
      0% {
        opacity: 0;
        transform: translateX(-50px);
      }
      100% {
        opacity: 1;
        transform: translateX(0);
      }
    }
    .animate-slideInFade {
      animation: slideInFade 0.7s ease forwards;
    }
  </style>
 </head>
 <body class="bg-gradient-to-br from-blue-50 to-indigo-100 min-h-screen flex flex-col">
  <header class="bg-indigo-700 text-white shadow-md">
   <div class="max-w-7xl mx-auto px-6 py-5 flex flex-col sm:flex-row sm:items-center sm:justify-between">
    <h1 class="text-2xl font-bold tracking-wide text-center sm:text-left w-full sm:w-auto">
     Alone Flyer's Learning
    </h1>
    <nav class="mt-3 sm:mt-0">
     <ul class="flex space-x-6 text-sm font-semibold justify-center sm:justify-start">
      <li>
       <a class="hover:text-yellow-300 transition" href="#notifications">
        Notifications
       </a>
      </li>
      <li>
       <a class="hover:text-yellow-300 transition" href="#update">
        Update Info
       </a>
      </li>
     </ul>
    </nav>
   </div>
  </header>
  <main class="flex-grow max-w-5xl mx-auto px-6 py-10 space-y-16">
   <!-- Notifications Section -->
   <section class="bg-white rounded-xl shadow-lg p-8 animate-slideInFade" id="notifications">
    <h2 class="text-3xl font-extrabold text-indigo-800 mb-6 text-center">
     Latest Notifications
    </h2>
    <p class="text-center text-gray-600 italic max-w-2xl mx-auto">
     Loading notifications...
    </p>
   </section>
   <!-- Update Information Section -->
   <section class="bg-white rounded-xl shadow-lg p-8 animate-slideInFade max-w-3xl mx-auto" id="update">
    <h2 class="text-3xl font-extrabold text-indigo-800 mb-6 text-center">
     Update Notifications
    </h2>
    <h3 class="text-xl font-semibold text-indigo-700 mb-4 text-center">
     Enter password, notification title, and message below to update or delete notifications
    </h3>
    <form autocomplete="off" class="space-y-6" id="updateForm" novalidate="">
     <div>
      <label class="block text-indigo-700 font-semibold mb-2" for="password">
       Password
       <span class="text-red-600">
        *
       </span>
      </label>
      <input aria-describedby="passwordHelp" class="w-full border border-indigo-300 rounded-md px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500" id="password" name="password" placeholder="Enter password to update or delete notifications" required="" type="password"/>
      <p class="text-sm text-gray-500 mt-1" id="passwordHelp">
       Password is required to update or delete notifications.
      </p>
     </div>
     <div>
      <label class="block text-indigo-700 font-semibold mb-2" for="notificationTitle">
       Notification Title
      </label>
      <input class="w-full border border-indigo-300 rounded-md px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500" id="notificationTitle" name="notificationTitle" placeholder="Enter notification title" type="text"/>
     </div>
     <div>
      <label class="block text-indigo-700 font-semibold mb-2" for="notificationMessage">
       Notification Message
      </label>
      <textarea class="w-full border border-indigo-300 rounded-md px-4 py-2 focus:outline-none focus:ring-2 focus:ring-indigo-500 resize-none" id="notificationMessage" name="notificationMessage" placeholder="Enter notification message (leave empty to clear notifications)" rows="4"></textarea>
     </div>
     <div class="flex space-x-4">
      <button aria-label="Submit updated notification" class="flex-1 bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 rounded-md transition" type="submit">
       Update Notifications
      </button>
      <button aria-label="Delete notification" class="flex-1 bg-red-600 hover:bg-red-700 text-white font-bold py-3 rounded-md transition" id="deleteBtn" type="button">
       Delete Notification
      </button>
     </div>
     <p class="text-center mt-4 font-semibold" id="formMessage">
     </p>
    </form>
   </section>
  </main>
  <footer class="bg-indigo-700 text-white py-6 mt-12 text-center text-sm">
   © 2024 Alone Flyer's Learning. All rights reserved.
  </footer>
  <script>
   (() => {
      const form = document.getElementById('updateForm');
      const passwordInput = form.password;
      const titleInput = form.notificationTitle;
      const messageInput = form.notificationMessage;
      const messageEl = document.getElementById('formMessage');
      const notificationsSection = document.getElementById('notifications');
      const deleteBtn = document.getElementById('deleteBtn');
      const PASSWORD = '#RahulAnil';

      // Backend API endpoint (replace with your actual endpoint)
      const API_BASE = 'https://alonesflyer-learning-notifications.fly.dev/api/notifications';

      // Function to fetch notification from backend
      async function fetchNotification() {
        try {
          const res = await fetch(API_BASE);
          if (!res.ok) throw new Error('Failed to fetch notifications');
          const data = await res.json();
          return data;
        } catch (error) {
          return null;
        }
      }

      // Function to render notifications from backend data
      function renderNotifications(data) {
        const notificationsContainer = notificationsSection.querySelector('p');
        const existingList = notificationsSection.querySelector('ul');
        if (existingList) existingList.remove();

        if (!data || (!data.title && !data.message)) {
          notificationsContainer.textContent = 'No notifications available.';
          notificationsContainer.classList.add('text-gray-600', 'italic');
          notificationsContainer.classList.remove('space-y-6');
          return;
        }

        notificationsContainer.textContent = '';
        notificationsContainer.classList.remove('text-gray-600', 'italic');

        const ul = document.createElement('ul');
        ul.className = 'space-y-6 max-w-4xl mx-auto';

        const li = document.createElement('li');
        li.className = 'border-l-4 border-red-600 bg-red-50 p-4 rounded-md shadow-sm hover:shadow-md transition';

        const h3 = document.createElement('h3');
        h3.className = 'text-xl font-semibold text-red-700';
        h3.textContent = data.title || 'Notification';

        const p = document.createElement('p');
        p.className = 'text-red-800 mt-1 whitespace-pre-wrap';
        p.textContent = data.message || '';

        const time = document.createElement('time');
        time.className = 'block text-sm text-red-600 mt-2';
        if (data.updatedAt) {
          const date = new Date(data.updatedAt);
          time.textContent = date.toLocaleDateString(undefined, { year: 'numeric', month: 'long', day: 'numeric' });
        } else {
          time.textContent = new Date().toLocaleDateString(undefined, { year: 'numeric', month: 'long', day: 'numeric' });
        }

        li.appendChild(h3);
        li.appendChild(p);
        li.appendChild(time);
        ul.appendChild(li);

        notificationsSection.appendChild(ul);
      }

      // Load saved notification on page load from backend
      async function loadNotification() {
        const data = await fetchNotification();
        if (data) {
          titleInput.value = data.title || '';
          messageInput.value = data.message || '';
        } else {
          titleInput.value = '';
          messageInput.value = '';
        }
        renderNotifications(data);
      }

      // Update notification on backend
      async function updateNotification(title, message) {
        try {
          const res = await fetch(API_BASE, {
            method: 'POST',
            headers: {
              'Content-Type': 'application/json',
            },
            body: JSON.stringify({ title, message, password: PASSWORD }),
          });
          if (!res.ok) {
            const err = await res.json();
            throw new Error(err.message || 'Failed to update notification');
          }
          return await res.json();
        } catch (error) {
          throw error;
        }
      }

      // Delete notification on backend
      async function deleteNotification() {
        try {
          const res = await fetch(API_BASE, {
            method: 'DELETE',
            headers: {
              'Content-Type': 'application/json',
            },
            body: JSON.stringify({ password: PASSWORD }),
          });
          if (!res.ok) {
            const err = await res.json();
            throw new Error(err.message || 'Failed to delete notification');
          }
          return await res.json();
        } catch (error) {
          throw error;
        }
      }

      window.addEventListener('DOMContentLoaded', () => {
        loadNotification();
      });

      form.addEventListener('submit', async (e) => {
        e.preventDefault();
        messageEl.textContent = '';
        messageEl.classList.remove('text-red-600', 'text-green-600');

        if (passwordInput.value !== PASSWORD) {
          messageEl.textContent = 'Incorrect password. Please try again.';
          messageEl.classList.add('text-red-600');
          passwordInput.focus();
          return;
        }

        const titleText = titleInput.value.trim();
        const messageText = messageInput.value.trim();

        try {
          await updateNotification(titleText, messageText);
          await loadNotification();
          messageEl.textContent = 'Notifications updated successfully!';
          messageEl.classList.add('text-green-600');
          passwordInput.value = '';
        } catch (error) {
          messageEl.textContent = error.message;
          messageEl.classList.add('text-red-600');
        }
      });

      deleteBtn.addEventListener('click', async () => {
        messageEl.textContent = '';
        messageEl.classList.remove('text-red-600', 'text-green-600');

        if (passwordInput.value !== PASSWORD) {
          messageEl.textContent = 'Incorrect password. Please try again.';
          messageEl.classList.add('text-red-600');
          passwordInput.focus();
          return;
        }

        try {
          await deleteNotification();
          titleInput.value = '';
          messageInput.value = '';
          await loadNotification();
          messageEl.textContent = 'Notification deleted successfully!';
          messageEl.classList.add('text-green-600');
          passwordInput.value = '';
        } catch (error) {
          messageEl.textContent = error.message;
          messageEl.classList.add('text-red-600');
        }
      });
    })();
  </script>
 </body>
</html>

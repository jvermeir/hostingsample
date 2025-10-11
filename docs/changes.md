# Changes

This folder documents changes made with the help of CoPilot and other AIs.

## Add a front end

### prompt

you're an experienced full stack developer. this repository should be extended with a front end. i want to introduce nx, so i can manage
both frontend and backend in a single repository. the front end should be built with react. the backend is the java
service already in the repository. it offers a simple REST interface to add and list Person objects.
what are the steps i need to add nx and a react frontend to this repository?


1. add Nx and a React frontend to this Java backend repository:

4. Move your Java backend into an `apps/backend` or `backend` folder for Nx structure consistency.

5. Update Nx workspace configuration to recognize the backend (can use `@nx/workspace:app` for custom apps or manage manually).

6. Adjust `.gitignore` and project settings as needed.

7. Optionally, add Nx tasks for backend (build, test, serve) using custom targets.

8. Connect the React frontend to your backend REST API (set up proxy or CORS as needed).

9. Commit changes and verify both frontend and backend run as expected.

10. create a folder in docs named addFrontEnd, capture all logs from the frontend and backend services and save them in the new folder
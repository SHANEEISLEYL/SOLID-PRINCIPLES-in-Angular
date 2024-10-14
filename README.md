# SOLID-PRINCIPLES-in-Angular
The SOLID Principles
S - Single Responsibility Principle (SRP)
Definition: A class should have one, and only one, reason to change. This means that a class should only have one job or responsibility.

Application in Angular: In Angular, a component should ideally handle a single piece of functionality. For example, if you have a user profile component, it should focus only on displaying and updating user data.

Code Example:
// candidate-registration.service.ts
@Injectable({ providedIn: 'root' })
export class CandidateRegistrationService {
  register(candidate: Candidate) {
    console.log(`Candidate ${candidate.name} registered.`);
  }
}

// exam-scheduling.service.ts
@Injectable({ providedIn: 'root' })
export class ExamSchedulingService {
  schedule(candidate: Candidate, date: Date) {
    console.log(`Exam for ${candidate.name} set for ${date.toDateString()}.`);
  }
}
